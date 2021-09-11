---
layout: post
title: Parallelization of PDL code
comments: true
excerpt: Experiments with PDL::ParallelCPU, thread_define and PP code.

tags:
   - pdl
   - perl
   - photonics
---


# Introduction

In a [previous post](https://wlmb.github.io/2021/09/03/Orthogonalization/) I developed some PDL codes for vectorizing
orthogonalization of basis sets, but the code had some flaws. In
particular, it wouldn't work in the presence of
paralelization. However, when I tried to check parallelizing the code,
PDL refused to launch parallel threads. I want to understand why, so I
do a few experiments here.


# Boilerplate code


## Initialization

    use warnings;
    use strict;
    use PDL;
    use v5.12;

    my $N=20; # size of vector
    set_autopthread_targ(4); # Number of cores in my laptop
    set_autopthread_size(0); # zero to attemp to parallelize small vectors
    my $x=sequence($N);


## Report

    say "Threads: ",get_autopthread_actual();
    say "Result: $x";


# Simple scalar routine


## Code

    <<initialization>>
    $x++;
    <<report>>


## Run it

    ./simple.pl


## Results

    Threads: 4
    Result: [1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20]

Seems ok.


# Same with `thread_define`


## Code

    <<initialization>>
    increment($x);
    <<report>>
    BEGIN {
        thread_define 'increment([io]a())', over {
    	$_[0]++;
        }
    }


## Run it

    ./thread_define.pl


## Results

    Threads: 0
    Result: [1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20]

I repeat but using an explicit vector instead of a scalar in the `thread_define`.


## Code

    <<initialization>>
    increment($x);
    <<report>>
    BEGIN {
        thread_define 'increment([io]a(n))', over {
    	$_[0]++;
        }
    }


## Run it

    ./thread_define_v.pl


## Results

    Threads: 4

Seems ok again. So implicit threading seems not to parallelize for
operations defined with `thread_define` but it does work for explicit
vector operations.

Now I try with a scalar and a separate output.


## Code

    <<initialization>>
    $y=null;
    increment($x, $y);
    $x=$y;
    <<report>>
    BEGIN {
        thread_define 'increment(a();[o]b())', over {
    	$_[1].=$_[0]+1;
        }
    }


## Run it

    ./thread_define_o.pl


## Results:

    Threads: 0
    Result: [1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20]

So it seems that when implicit threading a `thread_defined` function,
there is no parallelization even when input and output are separated.


# Inline::Pddlpp

Now I solve the same using `Inline::Pdlpp`.


## Code

    <<initialization>>
    $x->increment;
    <<report>>
    use Inline Pdlpp => <<'EOPP'
    pp_def('increment',
           Pars=>'[io]a()',
           Code=>'++$x();',
    );
    EOPP


## Run it

    ./pdlpp.pl


## Results

    Threads: 4
    Result: [1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20]

So the implicit threading for routines defined with Inline PDL does
parallelize.


# Dumb mistakes

Now I test the kind of dumb mistake that could happen when
parallelizing codes that modify their inputs, as mentioned in the
introduction.


## Example

Below is a code to perform partial sums of an array.

    perl -MList::Util=reductions -E 'say join " ", reductions {$a+$b} 0..19'


### Results

    0 1 3 6 10 15 21 28 36 45 55 66 78 91 105 120 136 153 171 190


## Same in PDL

    perl -MPDL -MPDL::NiceSlice -E '$x=sequence(20)->dummy(1,20);say +($x*($x->xvals<=$x->yvals))->sumover;'


### Results

    [0 1 3 6 10 15 21 28 36 45 55 66 78 91 105 120 136 153 171 190]


## The same with a complicated trick as in my [previous post. ](https://wlmb.github.io/2021/09/03/Orthogonalization/)


### Code

    use warnings;
    use strict;
    use v5.12;
    use PDL;
    use PDL::NiceSlice;
    my $x=sequence(20);
    sums($x);
    say $x;
    sub sums {
        $x=shift;
        $x->sums_aux($x->sequence(), $x);
    }
    no PDL::NiceSlice;
    use Inline Pdlpp => <<'EOPP'
        pp_def('sums_aux',
               Pars=>'[io]a(); p(); b(n)',
    	   Code=>q{
    		 PDL_Indx i=$p()-1;
    	         if(i>=0){$a()+=$b(n=>i);}
    		 },
        );
    EOPP


### Run it

    ./tricky.pl


### Results

    [0 1 3 6 10 15 21 28 36 45 55 66 78 91 105 120 136 153 171 190]

Tricky, but it works.


## Parallelized version.

I rewrite the same program, but I only print the last value (an error
in any previous value would produce an error in the last one), and I
accept an argument for the size of the sequence. I also print the
exact expected value. I explicitly use the longlong type, to test
large numbers.


### Code

    use warnings;
    use strict;
    use v5.12;
    use PDL;
    use PDL::NiceSlice;
    set_autopthread_targ(4);
    set_autopthread_size(0);
    my $N=shift @ARGV;
    my $x=sequence(longlong, $N);
    sums($x);
    say "Threads: ", get_autopthread_actual;
    say "Size of array: $N\nLast result: ", scalar $x((-1)), " vs. exact result: ", $N*($N-1)/2;
    sub sums {
        $x=shift;
        $x->sums_aux($x->sequence(), $x);
    }
    no PDL::NiceSlice;
    use Inline Pdlpp => <<'EOPP'
        pp_def('sums_aux',
               Pars=>'[io]a(); p(); b(n)',
    	   Code=>q{
    		   PDL_Indx i=$p()-1;
    	           if(i>=0){
    		     $a()+=$b(n=>i);
    		   }
    		},
        );
    EOPP


### Run it

    ./tricky_p.pl 20


### Results:

    Threads: 4
    Size of array: 20
    Last result: 190 vs. exact result: 190

This results look good, but&#x2026;


### Run it again

    ./tricky_p.pl 18000


### Results

    Threads: 4
    Size of array: 18000
    Last result: 151872749 vs. exact result: 161991000

So for large enough vectors, the parallelized version of the tricky
code yields the wrong result.


# Conclusion

It seems that `thread_define` doesn't parallelize iterations over
intrinsic dimensions, but Inline::Pdlpp does. And of course, if the
code is indeed parallelized, you shouldn't trust the results if they
depend on the order of execution, as in my tricky but dumb example
above. Thus, for the vectorizable orthogonalization trick presented in
my [previous post](https://wlmb.github.io/2021/09/03/Orthogonalization/), care should be taken to avoid its parallelization.
