---
layout: post
title: Orthogonalization of vector sets in PDL.
comments: true
excerpt: Implementation of orthogonalizations in the Perl Data Language.

tags:
   - pdl
   - perl
   - photonics
---


# Introduction

I have a code in my package for [Photonic and metamaterials calculations](https://github.com/wlmb/Photonic/)
to do some orthonormalization within Haydock iterations
for a large set of states. I use the standard Gram-Schmidt procedure,
which is iterative. For each vector, I substract its projections onto
the previous elements. I used to store each vector as an element in an
array, but after many modifications of the code, they are now part of
a large ndarray. Thus Ed (@mohawk2) suggested to vectorize the
procedure using PDL threading instead of PERL iterations. I thought it
is not possible, but here, I test a few alternatives.


# Gram Schmidt

The original version goes like this:

    # Gram Schmidt orthogonalization, iterative
    use warnings;
    use strict;
    use v5.12;
    use PDL;
    use PDL::NiceSlice;
    use Time::HiRes qw(time);

    $PDL::BIGPDL=1;
    my ($N,$M)=@ARGV; # dimensions of system
    die "Usage: ./gramschmidt N M with N>=M" unless defined $N && defined $M and $N>=$M;
    srand(0); # for reproducible tests.
    my $V=random($N,$M); # M random N-vectors.
    # The first index is the vector index i and the second the vector number: i,n
    my $t0=time();
    foreach my $m (0..$M-1){
        $V(:,($m))-= (($V(:,($m))*$V(:,0:$m-1))->sumover*($V(:,0:$m-1)->transpose))->sumover if $m>0;
        $V(:,($m))/=($V(:,($m))**2)->sumover->sqrt; #normalize
    }
    my $t1=time();
    say "Gram Schmidt time for $N,$M=", $t1-$t0;
    # Check orthonormality
    my $O=(($V->dummy(2)*$V->dummy(1))->sumover-identity($M))->abs->sum;
    say "Orthogonality=$O";
    my $t2=time();
    say "Total time: ", $t2-$t0;
    say $V if $N<=5;

This program builds a square array of random numbers which I interpret
as a collection of row vectors and then orthogonalizes them
iteratively using *|n'>=sum<sub>m<n</sub> |m><m|n>* and then normalizing *|n'>*.
I test it on a 1000x1000 matrix

    ./gramschmidt.pl 1000 1000

Results:

    Gram Schmidt time for 1000,1000=4.96293306350708
    Orthogonality=3.69626767899845e-08
    Total time: 10.2968249320984

Checking the orthogonality seems to take longer than the actual
orthogonalization, but in this example it requires building a large
1000x1000x1000 array.


# Modified Gram Schmidt

In the modified version after each step orthogonalizing, say, *|n>* to *|m>*,
building *|n'>=|n>-|m><m|n>*, I replace *|n>* by *|n'>* before
orthogonalizing to the next basis vector *|m+1>*. The results would
agree with the original procedure using infinite precision, but might
differ for finite precision.

    # Modified Gram Schmidt orthogonalization, iterative
    use warnings;
    use strict;
    use v5.12;
    use PDL;
    use PDL::NiceSlice;
    use Time::HiRes qw(time);

    $PDL::BIGPDL=1;
    my ($N,$M)=@ARGV; # dimensions of system
    die "Usage: ./gramschmidt N M with N>=M" unless defined $N && defined $M and $N>=$M;
    srand(0); # for reproducible tests.
    my $V=random($N,$M); # random vectors.
    # The first index is the vector index i and the second the vector number: i,m
    my $t0=time();
    foreach my $m (0..$M-1){
        foreach my $n (0..$m-1){
    	$V(:,($m))-=(($V(:,($m))*$V(:,($n)))->sumover*$V(:,($n)));
        }
        $V(:,($m))/=($V(:,($m))**2)->sumover->sqrt; #normalize
    }
    my $t1=time();
    say "Modified Gram Schmidt time for $N,$M=", $t1-$t0;
    # Check orthonormality
    my $O=(($V->dummy(2)*$V->dummy(1))->sumover-identity($M))->abs->sum;
    say "Orthogonality=$O";
    my $t2=time();
    say "Total time: ", $t2-$t0;
    say $V if $N<=5;

    ./modifiedgramschmidt.pl 1000 1000

Results:

    Modified Gram Schmidt time for 1000,1000=12.7265810966492
    Orthogonality=3.30134552816193e-10
    Total time: 17.4651801586151

The procedure is much slower, due to the nested PERL iteration, but
the precision is two orders of magnitude better.


# QR factorization

Using the Householder transformation, a matrix *V* may be decomposed
into the product *QR*, where *Q* is an orthogonal matrix and R is upper
triangular. Furthermore, the first *n* columns of *Q* span the same space
as the first *n* columns of *V*. Thus, *QR* factorization accomplishes an
orthogonalization of the columns of *V*. So, I'll try
my luck with the `mqr` routine from `PDL::LinearAlgebra.`

    # QR factorization
    use warnings;
    use strict;
    use v5.12;
    use PDL;
    use PDL::NiceSlice;
    use PDL::LinearAlgebra;
    use Time::HiRes qw(time);

    $PDL::BIGPDL=1;
    my ($N,$M)=@ARGV; # dimensions of system
    die "Usage: ./modifiedgramschmidt N M with N>=M" unless defined $N && defined $M and $N>=$M;
    srand(0); # for reproducible tests.
    my $V=random($N,$M); # random vectors.
    # The first index is the vector index i and the second the vector number: i,m
    my $t0=time();
    $V=mqr($V->transpose)->transpose; # from PDL::LinearAlgebra
    my $t1=time();
    say "QR time for $N,$M=", $t1-$t0;
    # Check orthonormality
    my $O=(($V->dummy(2)*$V->dummy(1))->sumover-identity($M))->abs->sum;
    say "Orthogonality=$O";
    my $t2=time();
    say "Total time: ", $t2-$t0;
    say $V if $N<=5;

    ./QR.pl 1000 1000

Results:

    QR time for 1000,1000=0.342689037322998
    Orthogonality=2.99989157025321e-11
    Total time: 7.1581711769104

The orthogonality became another order of magnitude better, and the
time gained one order of magnitude with respect to the first algorithm
and two with respect to the second one. So it seems this is the best
procedure for orthogonalization within PDL.

Now I do a case with a small number of entries to check that I get the
same result set of orthogonalized vectors. I also test sets with fewer
vectors than the space dimension, to make sure I didn't mix up dimensions.

    ./gramschmidt.pl 5 4
    ./modifiedgramschmidt.pl 5 4
    ./QR.pl 5 4

Results:

    Gram Schmidt time for 5,4=0.000535011291503906
    Orthogonality=3.12944115066216e-15
    Total time: 0.000841140747070312

    [
     [   0.1313358   0.57653872  0.074092339   0.66923001   0.44384178]
     [  0.87588479  -0.20720125   0.38458399   -0.1370171   0.15236453]
     [  -0.3739352   0.19733953   0.88397582  -0.19940276 0.0074073153]
     [  0.25173294   0.43494961  0.047217819   0.13603524  -0.85247537]
    ]

    Modified Gram Schmidt time for 5,4=0.000305891036987305
    Orthogonality=1.6531914726059e-15
    Total time: 0.000445842742919922

    [
     [   0.1313358   0.57653872  0.074092339   0.66923001   0.44384178]
     [  0.87588479  -0.20720125   0.38458399   -0.1370171   0.15236453]
     [  -0.3739352   0.19733953   0.88397582  -0.19940276 0.0074073153]
     [  0.25173294   0.43494961  0.047217819   0.13603524  -0.85247537]
    ]

    QR time for 5,4=0.000292062759399414
    Orthogonality=2.16840434497101e-15
    Total time: 0.000442981719970703

    [
     [   -0.1313358   -0.57653872  -0.074092339   -0.66923001   -0.44384178]
     [   0.87588479   -0.20720125    0.38458399    -0.1370171    0.15236453]
     [    0.3739352   -0.19733953   -0.88397582    0.19940276 -0.0074073153]
     [   0.25173294    0.43494961   0.047217819    0.13603524   -0.85247537]
    ]

Disregarding sign changes, all three methods yielded the same result.

Thus, although I didn't vectorize the code, the use of the Householder
transformation to do a QR factorization performs its iterations within a
`C` code, and thus is much faster, besides being a more stable and
accurate algorithm.

I'm still not sure this may be applied to `Photonic` as the product
between states is not a simple multiplication of vectors of
numbers.


# PDL::PP

Now I use PDL::PP to build a PDL program that interfaces directly to
C-like code. I implement below the modified Gram Schmidt algorithm.

    # Gram Schmidt orthogonalization, vectorized
    use warnings;
    use strict;
    use v5.12;
    use PDL;
    use PDL::NiceSlice;
    use PDL::PP;
    use Time::HiRes qw(time);

    $PDL::BIGPDL=1;
    my ($N,$M)=@ARGV; # dimensions of system
    die "Usage: ./modifiedgramschmidtv N M with N>=M" unless defined $N && defined $M and $N>=$M;
    srand(0); # for reproducible tests.
    my $V=random($N,$M); # M random N-vectors.
    # The first index is the vector index i and the second the vector number: i,n
    my $t0=time();
    $V->orthogonalize();
    my $t1=time();
    say "Modified GS PDL::PP time for $N,$M=", $t1-$t0;
    # Check orthonormality
    my $O=(($V->dummy(2)*$V->dummy(1))->sumover-identity($M))->abs->sum;
    say "Orthogonality=$O";
    my $t2=time();
    say "Total time: ", $t2-$t0;
    say $V if $N<=5;

    no PDL::NiceSlice;
    use Inline Pdlpp => <<'EOPP'
     pp_def('orthogonalize',
            Pars=>'[io] V(n,m);', # modify input matrix
            Code=>'
     	  loop(m)%{
     	      for(int l=0; l < m; ++l){
     		  $GENERIC() p=0; /* accumulator for inner product */
     		  loop(n) %{ /* component */
     		      p+=$V()*$V(m=>l); /* syntax is strange */
     		  %}
     		  loop(n) %{ /* subtract projection */
     		      $V()-=p*$V(m=>l);
     		  %}
     	      }
     	      $GENERIC() q=0;
     	      loop(n) %{ /* square magnitude */
     		  q+=$V()*$V();
     	      %}
     	      q=sqrt(q);
     	      loop(n) %{
     		  $V()/=q; /* normalize */
     	      %}
      	  %}
            ',
         );
    EOPP

    ./gramschmidt.pl 5 4
    ./modifiedgramschmidt.pl 5 4
    ./QR.pl 5 4
    ./modifiedgramschmidtv.pl 5 4

Results:

    Gram Schmidt time for 5,4=0.000308036804199219
    Orthogonality=3.12944115066216e-15
    Total time: 0.000442981719970703

    [
     [   0.1313358   0.57653872  0.074092339   0.66923001   0.44384178]
     [  0.87588479  -0.20720125   0.38458399   -0.1370171   0.15236453]
     [  -0.3739352   0.19733953   0.88397582  -0.19940276 0.0074073153]
     [  0.25173294   0.43494961  0.047217819   0.13603524  -0.85247537]
    ]

    Modified Gram Schmidt time for 5,4=0.000325202941894531
    Orthogonality=1.6531914726059e-15
    Total time: 0.000478029251098633

    [
     [   0.1313358   0.57653872  0.074092339   0.66923001   0.44384178]
     [  0.87588479  -0.20720125   0.38458399   -0.1370171   0.15236453]
     [  -0.3739352   0.19733953   0.88397582  -0.19940276 0.0074073153]
     [  0.25173294   0.43494961  0.047217819   0.13603524  -0.85247537]
    ]

    QR time for 5,4=0.000297069549560547
    Orthogonality=2.16840434497101e-15
    Total time: 0.000451087951660156

    [
     [   -0.1313358   -0.57653872  -0.074092339   -0.66923001   -0.44384178]
     [   0.87588479   -0.20720125    0.38458399    -0.1370171    0.15236453]
     [    0.3739352   -0.19733953   -0.88397582    0.19940276 -0.0074073153]
     [   0.25173294    0.43494961   0.047217819    0.13603524   -0.85247537]
    ]

    Modified GS PDL::PP time for 5,4=5.96046447753906e-06
    Orthogonality=1.6531914726059e-15
    Total time: 0.000267982482910156

    [
     [   0.1313358   0.57653872  0.074092339   0.66923001   0.44384178]
     [  0.87588479  -0.20720125   0.38458399   -0.1370171   0.15236453]
     [  -0.3739352   0.19733953   0.88397582  -0.19940276 0.0074073153]
     [  0.25173294   0.43494961  0.047217819   0.13603524  -0.85247537]
    ]

    ./gramschmidt.pl 1000 1000
    ./modifiedgramschmidt.pl 1000 1000
    ./QR.pl 1000 1000
    ./modifiedgramschmidtv.pl 1000 1000

Results:

    Gram Schmidt time for 1000,1000=4.89408993721008
    Orthogonality=3.69626767899845e-08
    Total time: 9.66118001937866
    Modified Gram Schmidt time for 1000,1000=12.8312540054321
    Orthogonality=3.30134552816193e-10
    Total time: 17.5760328769684
    QR time for 1000,1000=0.338634014129639
    Orthogonality=2.99989157025321e-11
    Total time: 6.98031520843506
    Modified GS PDL::PP time for 1000,1000=2.36270093917847
    Orthogonality=3.29437648148214e-10
    Total time: 7.08088278770447


# Vectorization with thread<sub>define</sub>

After much thought, I found a tricky way to vectorize the ordinary
Gram Schmidt orthogonalization. To that end I use `thread_define`, a
function that builds threadable perl functions. Thus I define an auxiliary
function that orthogonalizes one vector *A* to an orthonormal subset *0:p-1* of a set
of vectors *B*. I add a scalar parameter with the index *p*. The
routine modifies its input parameter *A*. Then I call this function
using the full set of vectors *V* that I want to
orthonormalize as an *nXm* ndarray as both *A* and *B*. Instead of a
scalar *p* I use a sequence of numbers *0..m-1*. The threading engine
of `PDL` than sets *p=0*, *A=V(:,0)* and normalizes it, then sets *p=1*,
*A=V(:,1)*, orthogonalizes it to the previous normalized vector and
normalizes it, then proceeds with *p=2,3&#x2026;m-1* orthogonalizing to all
the previously orthogonalized vectors. My expectation is that using
the threading engine may be faster than using `PERL` loops.

    # Gram Schmidt orthogonalization, vectorized
    use warnings;
    use strict;
    use v5.12;
    use PDL;
    use PDL::NiceSlice;
    use PDL::PP;
    use Time::HiRes qw(time);

    $PDL::BIGPDL=1;
    my ($N,$M)=@ARGV; # dimensions of system
    die "Usage: ./gramschmidtv N M with N>=M" unless defined $N && defined $M and $N>=$M;
    srand(0); # for reproducible tests.
    my $V=random($N,$M); # M random N-vectors.
    # The first index is the vector index i and the second the vector number: i,n
    my $t0=time();
    orthonormalize($V);
    my $t1=time();
    say "GS vectorized with thread_define time for $N,$M=", $t1-$t0;
    # Check orthonormality
    my $O=(($V->dummy(2)*$V->dummy(1))->sumover-identity($M))->abs->sum;
    say "Orthogonality=$O";
    my $t2=time();
    say "Total time: ", $t2-$t0;
    say $V if $N<=5;
    sub orthonormalize {
        my $V=shift;
        ortho_aux($V, sequence($V->dim(1)), $V);
    }
    BEGIN{
        thread_define 'ortho_aux([io]A(n); p(); B(n,m))', over {
        # Orthogonalize one vector A to the first p orthonormal vectors of B.
        # With threading it can orthogonalize an arbitrary set basis
        # Modifies first argument
        my($A, $p, $B)=@_;
        my $N=$B(:,0:$p-1); # assume already normalized
        $A-=(($A*$N)->sumover*$N->transpose)->sumover if $p>0;
        my $q=($A*$A)->sumover->sqrt;
        $A/=$q if $q!=0;
        };
    }

    ./gramschmidtv.pl 5 4
    ./gramschmidt.pl 5 4

To my surprise, given the confusing logic (the ndarray *B* is
gradually modified in situ as the argument *A* is modified), *it
worked!*

    ./gramschmidtv.pl 1000 1000
    ./gramschmidt.pl 1000 1000

Results:

    GS vectorized with thread_define time for 1000,1000=4.72058701515198
    Orthogonality=3.69307216405263e-08
    Total time: 10.2687690258026
    Gram Schmidt time for 1000,1000=4.92849779129028
    Orthogonality=3.69626767899845e-08
    Total time: 10.0826327800751

The result is as good (or as bad) as the first Gram Schmidt
program. It has the advantage that it may be easily generalized to arbitrary
inner products. It can also be easily modified to deal with the
modified Gram Schmidt algorithm.

Unfortunately, there was no speed increase compared with the
pure `PERL/PDL` code!


# Conclusion

The winner so far is still the QR factorization, but the PDL::PP
code is as good as the modified PDL Gram Schmidt algorithm and is
about 5 times faster for the 1000x1000 orthogonalization (I don't know
why the orthogonality is close but not identical). It would be
useful to be able to call `PERL,PDL` code from `PDL::PP` code to
implement more complex inner products, but I guess it won't be too easy.
The `thread_define` solution has the advantage that it can accomodate
a generalized inner products, but it seems it didn't yield a speed
increase.
