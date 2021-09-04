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

I have a code in my package for [Photonic and metamaterials calculations](https://github.com/wlmb/Photonic/)
to do some orthonormalization within Haydock iterations
for a large set of states. I use the standard Gram-Schmidt procedure,
which is iterative. For each vector, I substract its projections onto
the previous elements. I used to store each vector as an element in an
array, but after many modifications of the code, they are now part of
a large ndarray. Thus Ed (@mohawk2) suggested to vectorize the
procedure using PDL threading instead of PERL iterations. I told him I
believe it is not possible. Here, I test a few alternatives.

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
as a collection of row vectors. I test it on a 1000x1000 matrix

    ./gramschmidt.pl 1000 1000

Results:

    Gram Schmidt time for 1000,1000=4.96293306350708
    Orthogonality=3.69626767899845e-08
    Total time: 10.2968249320984

Checking the orthogonality seems to take longer than the actual
orthogonalization, but in this example it requires building a large
1000x1000x1000 array.

The modified Gram Schmidt

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

It seems that a QR factorization accomplishes the same. Thus I'll try
my luck with mqr from PDL::LinearAlgebra.

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

Results:

    Time for 5,4=0.000288963317871094
    Orthogonality=3.12944115066216e-15
    Total time: 0.000442981719970703

    [
     [   0.1313358   0.57653872  0.074092339   0.66923001   0.44384178]
     [  0.87588479  -0.20720125   0.38458399   -0.1370171   0.15236453]
     [  -0.3739352   0.19733953   0.88397582  -0.19940276 0.0074073153]
     [  0.25173294   0.43494961  0.047217819   0.13603524  -0.85247537]
    ]

    Time for 5,4=0.000342130661010742
    Orthogonality=1.6531914726059e-15
    Total time: 0.000490188598632812

    [
     [   0.1313358   0.57653872  0.074092339   0.66923001   0.44384178]
     [  0.87588479  -0.20720125   0.38458399   -0.1370171   0.15236453]
     [  -0.3739352   0.19733953   0.88397582  -0.19940276 0.0074073153]
     [  0.25173294   0.43494961  0.047217819   0.13603524  -0.85247537]
    ]

    Time for 5,4=0.000276088714599609
    Orthogonality=2.16840434497101e-15
    Total time: 0.000426054000854492

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

Now I use PDL::PP to build a PDL program that interfaces directly to C
code. I implement below the modified Gram Schmidt algorithm.

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
            Pars=>'[io] V(n,m);',
            Code=>'
     	  loop(m)%{
     	      for(int l=0; l < m; ++l){
     		  $GENERIC() p=0;
     		  loop(n) %{
     		      p+=$V()*$V(m=>l);
     		  %}
     		  loop(n) %{
     		      $V()-=p*$V(m=>l);
     		  %}
     	      }
     	      $GENERIC() q=0;
     	      loop(n) %{
     		  q+=$V()*$V();
     	      %}
     	      q=sqrt(q);
     	      loop(n) %{
     		  $V()/=q;
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

Thus the winner so far is still the QR factorization, but the PDL::PP
code is as good as the modified PDL Gram Schmidt algorithm and is
about 5 times faster for the 1000x1000 orthogonalization. I don't know
why the orthogonality is close but not identical.
