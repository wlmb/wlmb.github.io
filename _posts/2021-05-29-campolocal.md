---
layout: post
title: Efecto de campo local superficial
comments: true
excerpt: Teoría del efecto de campo local superficial. Algunas notas para un curso sobre epióptica.
tags:
   - physics
   - surfaces
---


# Introducción

 ( Si encuentra las ecuaciones ilegibles en esta versión, puede
consultar la versión pdf con las ecuaciones bien tipografiadas
[aquí](/assets/pdf/20210529campolocal.pdf) )

La respuesta macroscópica de un sistema no es el simple promedio de su
respuesta microscópica. Esto se debe a que el campo eléctrico
microscópico tiene fluctuaciones espaciales que están correlacionadas
con la textura espacial del sistema. Este efecto es conocido como el
*efecto de campo local*. Un ejemplo muy conocido de este efecto es el
de un sólido isotrópico modelado como una red cúbica de entidades
polarizables puntuales caracterizadas por su polarizabilidad
<img src="/assets/ltximg/2021-05-29-campolocal_f06f20dee81ab8248628631211abcbe3c7ee9a80.png" alt="2021-05-29-campolocal_f06f20dee81ab8248628631211abcbe3c7ee9a80.png" />. Sin efecto de campo local, la respuesta dieléctrica
macroscópica sería


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_3e0ecd39deae07f68899706197251b8b4f08e2dc.png" alt="2021-05-29-campolocal_3e0ecd39deae07f68899706197251b8b4f08e2dc.png" />
</span>
<span class="equation-label">
1
</span>
</div>

con <img src="/assets/ltximg/2021-05-29-campolocal_58199a5456c6af107f6ae48293c635a1c794b09c.png" alt="2021-05-29-campolocal_58199a5456c6af107f6ae48293c635a1c794b09c.png" /> la densidad de
las entidades polarizables. Sin embargo, al tomar en cuenta que la
polarizabilidad es la respuesta no sólo al campo externo, sino también
al campo producido por todos los dipolos vecinos, la ecuación anterior
se ve reemplazada por la relación de Claussius-Mossoti,


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_73135f54abebe967ab72ab3e64a40f21e1a8d9ee.png" alt="2021-05-29-campolocal_73135f54abebe967ab72ab3e64a40f21e1a8d9ee.png" />
</span>
<span class="equation-label">
2
</span>
</div>


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_6e86be3f200a33a9bc9e35a5f830baa58418c191.png" alt="2021-05-29-campolocal_6e86be3f200a33a9bc9e35a5f830baa58418c191.png" />
</span>
<span class="equation-label">
3
</span>
</div>

Como la corrección de campo local depende de la interacción con
entidades polarizables vecinas, podríamos esperar que se vea
modificada en la vecindad de una superficie. El propósito de estas
notas es mostrar cómo podríamos calcular el efecto de campo local
superficial y explorar sus consecuencias.


# Teoría

Consideremos una red de Bravais bidimensional <img src="/assets/ltximg/2021-05-29-campolocal_5bd063f08144ad99558f0a7157e8c6078d6b815a.png" alt="2021-05-29-campolocal_5bd063f08144ad99558f0a7157e8c6078d6b815a.png" /> en el plano
<img src="/assets/ltximg/2021-05-29-campolocal_adf8662bae1b46aa38b626568e162ef56c7e11ff.png" alt="2021-05-29-campolocal_adf8662bae1b46aa38b626568e162ef56c7e11ff.png" /> ocupada por
cargas puntuales unitarias <img src="/assets/ltximg/2021-05-29-campolocal_3f8c539dd8aa8f627909271d43e4e37d0094eef2.png" alt="2021-05-29-campolocal_3f8c539dd8aa8f627909271d43e4e37d0094eef2.png" />. El potencial electrostático
<img src="/assets/ltximg/2021-05-29-campolocal_d21d844468ea5a5c9bc532fa537952b9c9c42b87.png" alt="2021-05-29-campolocal_d21d844468ea5a5c9bc532fa537952b9c9c42b87.png" /> que
produciría en un punto <img src="/assets/ltximg/2021-05-29-campolocal_245db958c78a5f721d51f4241c0090bf048fdf4b.png" alt="2021-05-29-campolocal_245db958c78a5f721d51f4241c0090bf048fdf4b.png" /> es


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_6a1d30764eb16698009f0ad68c5f61a9bf01883d.png" alt="2021-05-29-campolocal_6a1d30764eb16698009f0ad68c5f61a9bf01883d.png" />
</span>
<span class="equation-label">
4
</span>
</div>

La ecuación previa no es muy útil por la lenta convergencia en el
espacio real del potencial Coulombiano. Conviene entonces recurrir a la
ecuación diferencial del potencial,


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_35677304c526c65df6e95a2245c8ba2f7f04b026.png" alt="2021-05-29-campolocal_35677304c526c65df6e95a2245c8ba2f7f04b026.png" />
</span>
<span class="equation-label">
5
</span>
</div>

en el espacio recíproco <img src="/assets/ltximg/2021-05-29-campolocal_ca99b1d2c197d62429b20b2e07f1d43f9982386c.png" alt="2021-05-29-campolocal_ca99b1d2c197d62429b20b2e07f1d43f9982386c.png" /> definido por <img src="/assets/ltximg/2021-05-29-campolocal_5832a5dcfb21fcb6b7aea9822cda13ee31f0bbfb.png" alt="2021-05-29-campolocal_5832a5dcfb21fcb6b7aea9822cda13ee31f0bbfb.png" />,


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_2a9132df74afbca1440bcd94b1e882bb86a637d7.png" alt="2021-05-29-campolocal_2a9132df74afbca1440bcd94b1e882bb86a637d7.png" />
</span>
<span class="equation-label">
6
</span>
</div>

con <img src="/assets/ltximg/2021-05-29-campolocal_06b0064c464f9c3ff4ebfd5c657323cf3a067d9a.png" alt="2021-05-29-campolocal_06b0064c464f9c3ff4ebfd5c657323cf3a067d9a.png" /> es el coeficiente de Fourier 2D del potencial
<img src="/assets/ltximg/2021-05-29-campolocal_d21d844468ea5a5c9bc532fa537952b9c9c42b87.png" alt="2021-05-29-campolocal_d21d844468ea5a5c9bc532fa537952b9c9c42b87.png" /> evaluado a la altura <img src="/assets/ltximg/2021-05-29-campolocal_87596482ce53325ca7d4bd470c6fbdc163cfb5a7.png" alt="2021-05-29-campolocal_87596482ce53325ca7d4bd470c6fbdc163cfb5a7.png" />.
La solución que decae al alejarnos del plano <img src="/assets/ltximg/2021-05-29-campolocal_adf8662bae1b46aa38b626568e162ef56c7e11ff.png" alt="2021-05-29-campolocal_adf8662bae1b46aa38b626568e162ef56c7e11ff.png" /> para <img src="/assets/ltximg/2021-05-29-campolocal_02e5d3c38c08a90159a6d4ee5037f30f7e5181cc.png" alt="2021-05-29-campolocal_02e5d3c38c08a90159a6d4ee5037f30f7e5181cc.png" /> es


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_10a3822d3c72d38b0f50d19bff483af87953eb59.png" alt="2021-05-29-campolocal_10a3822d3c72d38b0f50d19bff483af87953eb59.png" />
</span>
<span class="equation-label">
7
</span>
</div>

Regresando al espacio real, el potencial queda dado por


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_0078513d6cd5dfde1455f57b9c2c0815b3860607.png" alt="2021-05-29-campolocal_0078513d6cd5dfde1455f57b9c2c0815b3860607.png" />
</span>
<span class="equation-label">
8
</span>
</div>

donde añadimos al termino <img src="/assets/ltximg/2021-05-29-campolocal_8b524674698b2174331edbb50aa5755e605322b1.png" alt="2021-05-29-campolocal_8b524674698b2174331edbb50aa5755e605322b1.png" /> correspondiente al potencial producido
por una película uniformemente cargada, y dónde introdujimos los
vectores


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_ba255325731d2f9240a249cdaf65d236796bd2e6.png" alt="2021-05-29-campolocal_ba255325731d2f9240a249cdaf65d236796bd2e6.png" />
</span>
<span class="equation-label">
9
</span>
</div>

y empleamos el signo <img src="/assets/ltximg/2021-05-29-campolocal_f91998fc131e577beb667681882370ddce95c855.png" alt="2021-05-29-campolocal_f91998fc131e577beb667681882370ddce95c855.png" /> cuando <img src="/assets/ltximg/2021-05-29-campolocal_dd60e5a847ef19e198dfda430bad84b6395521a4.png" alt="2021-05-29-campolocal_dd60e5a847ef19e198dfda430bad84b6395521a4.png" /> y el signo <img src="/assets/ltximg/2021-05-29-campolocal_468865871d0a1477f3412bcd09e73bbc72797741.png" alt="2021-05-29-campolocal_468865871d0a1477f3412bcd09e73bbc72797741.png" /> cuando
<img src="/assets/ltximg/2021-05-29-campolocal_1d735b9bca1aba8f58c8a18a98f3681713f8452a.png" alt="2021-05-29-campolocal_1d735b9bca1aba8f58c8a18a98f3681713f8452a.png" />. Esta es una serie rápidamente convergente siempre y cuando
<img src="/assets/ltximg/2021-05-29-campolocal_0593ea6674b560b1eb4caca0153e4e89ba43a996.png" alt="2021-05-29-campolocal_0593ea6674b560b1eb4caca0153e4e89ba43a996.png" />.

Consideremos ahora la misma red de Bravais, pero ocupada por
dipolos idénticos <img src="/assets/ltximg/2021-05-29-campolocal_93058fc8e37a7a3782b358c6cdf9de825f57dfe1.png" alt="2021-05-29-campolocal_93058fc8e37a7a3782b358c6cdf9de825f57dfe1.png" />. La densidad de carga sería entonces


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_7dc5164201c4dd8c1e07f36d87d75a73d01c386e.png" alt="2021-05-29-campolocal_7dc5164201c4dd8c1e07f36d87d75a73d01c386e.png" />
</span>
<span class="equation-label">
10
</span>
</div>

i.e., operamos sobre la densidad monopolar con el operador <img src="/assets/ltximg/2021-05-29-campolocal_100d471bdd248589d2ab2bb17b6484e5e191ce5d.png" alt="2021-05-29-campolocal_100d471bdd248589d2ab2bb17b6484e5e191ce5d.png" />. Luego,
el potencial dipolar <img src="/assets/ltximg/2021-05-29-campolocal_ffa97778ce04ddeb2dd26bf46f1ef9cbbc8d31dc.png" alt="2021-05-29-campolocal_ffa97778ce04ddeb2dd26bf46f1ef9cbbc8d31dc.png" /> se obtiene aplicando el mismo
operador sobre el potencial monopolar, <img src="/assets/ltximg/2021-05-29-campolocal_ace97a11986c0dc0081c3edc613c9b9a5a2c5f20.png" alt="2021-05-29-campolocal_ace97a11986c0dc0081c3edc613c9b9a5a2c5f20.png" />,


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_edfd09360292afba65e9b2962900eb438e00a3a9.png" alt="2021-05-29-campolocal_edfd09360292afba65e9b2962900eb438e00a3a9.png" />
</span>
<span class="equation-label">
11
</span>
</div>

y el campo eléctrico <img src="/assets/ltximg/2021-05-29-campolocal_f6cc90dac529e4a22efc531d6239dab3c04b1ce0.png" alt="2021-05-29-campolocal_f6cc90dac529e4a22efc531d6239dab3c04b1ce0.png" />,


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_956ed19ef0cd6b720caafa547f8cb7ab240ff297.png" alt="2021-05-29-campolocal_956ed19ef0cd6b720caafa547f8cb7ab240ff297.png" />
</span>
<span class="equation-label">
12
</span>
</div>

Construyamos ahora un cristal con caras planas orientadas de acuerdo a
alguna dirección cristalográfica.
La ecuación que obedece la -ésima entidad
polarizable es


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_91479f064a44d251206ab7a0aa18da0ff257dfdb.png" alt="2021-05-29-campolocal_91479f064a44d251206ab7a0aa18da0ff257dfdb.png" />
</span>
<span class="equation-label">
13
</span>
</div>

donde <img src="/assets/ltximg/2021-05-29-campolocal_8ba83390c2f67c25e1aecef0033f9ecfb3fc7b31.png" alt="2021-05-29-campolocal_8ba83390c2f67c25e1aecef0033f9ecfb3fc7b31.png" /> representa el campo eléctrico en el
sitio <img src="/assets/ltximg/2021-05-29-campolocal_802f985f8a255b1976f3886fa2d0c180979dd84c.png" alt="2021-05-29-campolocal_802f985f8a255b1976f3886fa2d0c180979dd84c.png" /> producido por un dipolo que <img src="/assets/ltximg/2021-05-29-campolocal_eb8c59938c801ac6c33df268718d10c7f3bf498f.png" alt="2021-05-29-campolocal_eb8c59938c801ac6c33df268718d10c7f3bf498f.png" /> en el sitio
<img src="/assets/ltximg/2021-05-29-campolocal_cae2d4d31c691e645c5b4eb88ae07cc3b4c5825f.png" alt="2021-05-29-campolocal_cae2d4d31c691e645c5b4eb88ae07cc3b4c5825f.png" />. Suponiendo que todos los dipolos de un plano son equivalentes,
podemos  podemos sumar las interacciones por planos
cristalinos. Definimos entonces


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_6857f5517101af444c2be2d8adf1505a229c7f92.png" alt="2021-05-29-campolocal_6857f5517101af444c2be2d8adf1505a229c7f92.png" />
</span>
<span class="equation-label">
14
</span>
</div>

donde <img src="/assets/ltximg/2021-05-29-campolocal_802f985f8a255b1976f3886fa2d0c180979dd84c.png" alt="2021-05-29-campolocal_802f985f8a255b1976f3886fa2d0c180979dd84c.png" /> es un sitio cualquiera del plano <img src="/assets/ltximg/2021-05-29-campolocal_58199a5456c6af107f6ae48293c635a1c794b09c.png" alt="2021-05-29-campolocal_58199a5456c6af107f6ae48293c635a1c794b09c.png" />. Usando el campo
dipolar previo,
la interacción entre planos cristalinos está dada por el tensor


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_66dd8b87e9a2253b8bdb8e24fef6ed7f5f0af22e.png" alt="2021-05-29-campolocal_66dd8b87e9a2253b8bdb8e24fef6ed7f5f0af22e.png" />
</span>
<span class="equation-label">
15
</span>
</div>

donde <img src="/assets/ltximg/2021-05-29-campolocal_7e6baf5ed4d02877a23853fc7409ffba0c4bd99d.png" alt="2021-05-29-campolocal_7e6baf5ed4d02877a23853fc7409ffba0c4bd99d.png" /> son vectores recíprocos bidimensionales, <img src="/assets/ltximg/2021-05-29-campolocal_431928413284600f006cc291fd3f4f67472baf33.png" alt="2021-05-29-campolocal_431928413284600f006cc291fd3f4f67472baf33.png" /> es
un vector que va de un sitio del plano <img src="/assets/ltximg/2021-05-29-campolocal_b2c1faafe389054fb76ed2f22fee4e477bf9270f.png" alt="2021-05-29-campolocal_b2c1faafe389054fb76ed2f22fee4e477bf9270f.png" /> a uno del plano <img src="/assets/ltximg/2021-05-29-campolocal_5f4e7b21a3ea44a39e70d22eda9e647299e9fdd7.png" alt="2021-05-29-campolocal_5f4e7b21a3ea44a39e70d22eda9e647299e9fdd7.png" />, y
donde usamos el signo <img src="/assets/ltximg/2021-05-29-campolocal_f91998fc131e577beb667681882370ddce95c855.png" alt="2021-05-29-campolocal_f91998fc131e577beb667681882370ddce95c855.png" /> cuando <img src="/assets/ltximg/2021-05-29-campolocal_e83c1e3c5a1329ebf295197f46574b8d54e3e56b.png" alt="2021-05-29-campolocal_e83c1e3c5a1329ebf295197f46574b8d54e3e56b.png" /> y el signo <img src="/assets/ltximg/2021-05-29-campolocal_468865871d0a1477f3412bcd09e73bbc72797741.png" alt="2021-05-29-campolocal_468865871d0a1477f3412bcd09e73bbc72797741.png" /> cuando <img src="/assets/ltximg/2021-05-29-campolocal_bba2d0c3bdc650d1475f9056469f1c20200759fa.png" alt="2021-05-29-campolocal_bba2d0c3bdc650d1475f9056469f1c20200759fa.png" />.
Para el caso <img src="/assets/ltximg/2021-05-29-campolocal_262ff47c938b92dc26114f00b931aa4e081b2a88.png" alt="2021-05-29-campolocal_262ff47c938b92dc26114f00b931aa4e081b2a88.png" /> podemos usar la regla de suma


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_fbf711bdd9852efa832e6ee4053d189fc9a51ddb.png" alt="2021-05-29-campolocal_fbf711bdd9852efa832e6ee4053d189fc9a51ddb.png" />
</span>
<span class="equation-label">
16
</span>
</div>

en el bulto del sistema, con <img src="/assets/ltximg/2021-05-29-campolocal_58199a5456c6af107f6ae48293c635a1c794b09c.png" alt="2021-05-29-campolocal_58199a5456c6af107f6ae48293c635a1c794b09c.png" /> la densidad de entidades
polarizables, y despejar <img src="/assets/ltximg/2021-05-29-campolocal_2759b2d6a699190ea40c868b682c1af506157c8e.png" alt="2021-05-29-campolocal_2759b2d6a699190ea40c868b682c1af506157c8e.png" /> (sin suma), la autointeracción
dipolar de un plano.


# Interacciones

Empezamos por cargar librerías y opciones.

    # name: init
    use strict;
    use warnings;
    use v5.12;

    use Getopt::Long; # Read options
    use Scalar::Util qw(looks_like_number);
    use Exporter::Renaming;
    use List::Util Renaming=>[all=>'lu_all']; # Rename all method

    use PDL;  # Perl Data Language
    use PDL::NiceSlice;
    use PDL::Constants qw(PI);

Necesitamos una rutina para mandar mensajes de error y medio explicar el uso del programa.

    # name: usage
    sub usage($$) {
        my ($options, $message)=@_;
        say $message;
        say $options;
        exit 1;
    }

También requrimos algunas rutinas de utilería. Definimos el producto
escalar (no hermitiano) entre vectores posiblemente
complejos. (La rutina de `PDL` no sabe aún qué hacer con complejos)

    # name: cinner
    sub cinner($$) {
        my ($a,$b)=@_;
        return ($a*$b)->sumover;
    }

Otra rutina de utilería para acotar el número de dígitos
decimales a imprimir.

    # name: trunc
    sub trunc($@) {
        my $size=shift; # how many decimal digits to keep
        my @a=map {s{(\.\d{$size})\d*}{$1}g; s{[ ]+}{  }g; $_}
                  map {sprintf "%s", $_} @_;
        return @a;
    }

Define, lee y valida parámetros de la línea de comandos.

    # name: parameters
    my ($a,$b); # 2D basis.
    my $c;  # 3D Separation between sites in nearby planes
    my $pqmax;   # index of largest reciprocal vector
    my $dmax;   # index of largest distance to calculate
    my $N; # seminumber of planes of film
    my $digits=7; # number of decimal digits to print
    my $options=q(
        'a=s'=>\$a, # 2D basis vector x,y
        'b=s'=>\$b, # 2D basis vector x,y
        'c=s'=>\$c, # 3D separation x,y,z
        'pqmax=i'=>\$pqmax,  # index of largest reciprocal vector
        'dmax=i'=>\$dmax,  # index of largest distance to calculate
        'N=i'=>\$N, # seminumber of planes of film
        'digits=i'=>\$digits, # number of decimal digits to print
        );
    my %options=(eval $options);
    die "Bad option definition: $@" if $@;
    GetOptions(%options) or usage $options, "Bad options";
    usage $options, "Undefined parameters"
          unless lu_all {defined $_} ($a, $b, $c, $pqmax, $dmax, $N);
    usage $options, "Vectors should be comma separated list of numbers"
          unless lu_all {looks_like_number $_} map {split ','} ($a, $b, $c);
    #convert from strings to vectors
    ($a,$b,$c) = map {pdl(split ',', $_)} ($a, $b, $c);
    usage $options, "Basis vectors should be 2D"
          unless lu_all {$_->dims==1 and $_->dim(0)==2} ($a, $b);
    usage $options, "c should be 3D" unless $c->dims==1 and $c->dim(0)==3;
    usage $options, "Third component of c should be positive"
          unless $c->((2)) > 0;
    usage $options, "pqmax should be positive" unless $pqmax > 0;
    usage $options, "dmax should be positive" unless $dmax > 0;
    usage $options, "N should be positive" unless $N > 0;

Calcula el área de la celda unitaria 2D <img src="/assets/ltximg/2021-05-29-campolocal_c3dc570205163ecb76c7206a14462fa66c686ba8.png" alt="2021-05-29-campolocal_c3dc570205163ecb76c7206a14462fa66c686ba8.png" />, el volumen de la celda
unitaria 3D <img src="/assets/ltximg/2021-05-29-campolocal_d6c0b8bdc1aa19f4b2ddb91aba07957479f16b0f.png" alt="2021-05-29-campolocal_d6c0b8bdc1aa19f4b2ddb91aba07957479f16b0f.png" /> y la densidad

    # name: area
    my $A=($a->((0))*$b->((1))-$a->((1))*$b->((0)))->abs;
    my $V=$A*$c->((2));
    my $density=1/$V;

Genera la red recíproca <img src="/assets/ltximg/2021-05-29-campolocal_dd312f024d9d9a8f9061b24d9ef1df5a1bbab291.png" alt="2021-05-29-campolocal_dd312f024d9d9a8f9061b24d9ef1df5a1bbab291.png" />, donde
<img src="/assets/ltximg/2021-05-29-campolocal_30545d589a777bee8a835bc4e86f74645922db70.png" alt="2021-05-29-campolocal_30545d589a777bee8a835bc4e86f74645922db70.png" /> son los elementos de la base dual,
<img src="/assets/ltximg/2021-05-29-campolocal_6777fd1faa1343238392c6534cabcd2091620b06.png" alt="2021-05-29-campolocal_6777fd1faa1343238392c6534cabcd2091620b06.png" />. En 2D,
<img src="/assets/ltximg/2021-05-29-campolocal_6c63c3cdb7830829d787fad0917d06d3e2318018.png" alt="2021-05-29-campolocal_6c63c3cdb7830829d787fad0917d06d3e2318018.png" /> y
<img src="/assets/ltximg/2021-05-29-campolocal_980ce7c651e278f41b1fe3e6cfbe822c461d31d8.png" alt="2021-05-29-campolocal_980ce7c651e278f41b1fe3e6cfbe822c461d31d8.png" />. En el programa
uso `$a` y `$b` para denotar la base y `$Ga$ y ~$Gb` para la base
dual.

    # name: reciprocal
    my ($a_perp, $b_perp)=map {pdl(-$_->((1)), $_->((0)))} ($a, $b);
    my ($Ga, $Gb)=map {2*PI*$_->[0]/inner($_->[0], $_->[1])}
    		  ([$b_perp, $a], [$a_perp, $b]);
    my $pq=zeroes(2*$pqmax+1,2*$pqmax+1)->ndcoords-$pqmax; #i,p,q
    my $G=$pq->((0),*1)*$Ga+$pq->((1),*1)*$Gb;  #i,p,q

Genera los vectores 3D <img src="/assets/ltximg/2021-05-29-campolocal_e60c17485333c40edba243d1f568a7ec0ceb4b7b.png" alt="2021-05-29-campolocal_e60c17485333c40edba243d1f568a7ec0ceb4b7b.png" />.

    # name: reciprocal-decay
    my $G_abs=inner($G, $G)->sqrt; # p,q
    my ($g_p, $g_m)=map {append($G, ($_*i()*$G_abs)->(*1))} (+1,-1); # i,p,q

Con ellos arma los tensores <img src="/assets/ltximg/2021-05-29-campolocal_09391bc92c22ef711b335f720de32f8e57851041.png" alt="2021-05-29-campolocal_09391bc92c22ef711b335f720de32f8e57851041.png" />.

    # name: T+-
    # i,j,gx,gy
    my ($T_p, $T_m)= map {-2*PI/$A*$_->(*1,:)*$_->(:,*1)/$G_abs->(*1,*1)}
    		     ($g_p, $g_m); # i,j,p,q
    $_->(:,:,$pqmax,$pqmax).=0 foreach ($T_p, $T_m); # Fix division by 0

Ahora arma las interacciones <img src="/assets/ltximg/2021-05-29-campolocal_c0fa0481baa7fd6562d1bdcdce41c3adb54a8186.png" alt="2021-05-29-campolocal_c0fa0481baa7fd6562d1bdcdce41c3adb54a8186.png" /> para <img src="/assets/ltximg/2021-05-29-campolocal_58199a5456c6af107f6ae48293c635a1c794b09c.png" alt="2021-05-29-campolocal_58199a5456c6af107f6ae48293c635a1c794b09c.png" /> positiva y negativa.

    # name: interactions
    my $ns=sequence($dmax)+1; # n
    my $exp_p=exp(i()*cinner($g_p, $c))**$ns->(*1,*1);   #p,q,n
    my $exp_m=exp(-i()*cinner($g_m, $c))**$ns->(*1,*1);  #p,q,n
    my $T_n0=($T_p #i,j,p,q
                 *$exp_p->(*1,*1)) #i,j,p,q,n
        ->mv(-2,0)->sumover->mv(-2,0)->sumover; #i,j,n
    my $T_mn0=($T_m #i,j,p,q
                  *$exp_m->(*1,*1)) #i,j,p,q,n
        ->mv(-2,0)->sumover->mv(-2,0)->sumover; #i,j,n

Usa la regla de suma de las interacciones dipolares para obtener la
autointeracción.

    # name: selfinteraction
    my $T_00 = 4*PI*$density/3*pdl([1,0,0],[0,1,0],[0,0,-2]) -
        $T_n0->mv(-1,0)->sumover - $T_mn0->mv(-1,0)->sumover;

Arma las interacciones <img src="/assets/ltximg/2021-05-29-campolocal_ccf8b85359e143162f4a3cd9b5a12d98c49b1cf6.png" alt="2021-05-29-campolocal_ccf8b85359e143162f4a3cd9b5a12d98c49b1cf6.png" /> por bloques para una película
con <img src="/assets/ltximg/2021-05-29-campolocal_c3f4119690053f995a5855a131cc753f5321b79d.png" alt="2021-05-29-campolocal_c3f4119690053f995a5855a131cc753f5321b79d.png" /> planos. `T_all` tiene la interacción <img src="/assets/ltximg/2021-05-29-campolocal_ec0deedd52537719709b3abf5919e0056b4b5494.png" alt="2021-05-29-campolocal_ec0deedd52537719709b3abf5919e0056b4b5494.png" /> en el sitio
`$N2+$n`.

    # name: interactions-film
    my $N2=2*$N+1; # Number of planes
    my $T_all=zeroes(cdouble, 3,3,2*$N2+1);
    $T_all->(:,:,$N2+1:$N2+$dmax).=$T_n0;
    $T_all->(:,:,$N2-1:$N2-$dmax).=$T_mn0;
    $T_all->(:,:,($N2)).=$T_00;
    my $T_nm=zeroes(cdouble,3,3,$N2,$N2);
    for my $n(0..$N2-1){
        for my $m(0..$N2-1){
            $T_nm->(:,:,($n),($m)).=$T_all(:,:,($n-$m+$N2));
        }
    }

Arma las interacciones faltantes para la misma película. Estas son
<img src="/assets/ltximg/2021-05-29-campolocal_5f769a67b8337032e1beae92b101ace06c44667e.png" alt="2021-05-29-campolocal_5f769a67b8337032e1beae92b101ace06c44667e.png" /> para <img src="/assets/ltximg/2021-05-29-campolocal_8855477fe2b44285bd474a3879ca21c992ab70c7.png" alt="2021-05-29-campolocal_8855477fe2b44285bd474a3879ca21c992ab70c7.png" /> menor a cero o <img src="/assets/ltximg/2021-05-29-campolocal_8855477fe2b44285bd474a3879ca21c992ab70c7.png" alt="2021-05-29-campolocal_8855477fe2b44285bd474a3879ca21c992ab70c7.png" /> mayor al ancho de la
película. Entonces, para los sitios <img src="/assets/ltximg/2021-05-29-campolocal_d41cce6e3488a04ffa2a9296fcf63634c1c143ba.png" alt="2021-05-29-campolocal_d41cce6e3488a04ffa2a9296fcf63634c1c143ba.png" />, <img src="/assets/ltximg/2021-05-29-campolocal_6041f74ea3c59c81eef71b47b696301daff9eebc.png" alt="2021-05-29-campolocal_6041f74ea3c59c81eef71b47b696301daff9eebc.png" /> y
para los sitios <img src="/assets/ltximg/2021-05-29-campolocal_4a544aa9363ad3f095200e6a3f9d91241250ac6d.png" alt="2021-05-29-campolocal_4a544aa9363ad3f095200e6a3f9d91241250ac6d.png" />, <img src="/assets/ltximg/2021-05-29-campolocal_b00f14c72846ed2f42703ed0707d876669fc5b84.png" alt="2021-05-29-campolocal_b00f14c72846ed2f42703ed0707d876669fc5b84.png" />, correspondientes a
los rangos `$N2+$n1+1:2*$N2` y `0:$n` de `$T_all`.

    # name: missing
    my $M_n=zeroes(cdouble,3,3,$N2);
    for my $n(0..$N2-1){
        $M_n->(:,:,($n)).=
            $T_all->(:,:,$N2+$n+1:2*$N2)->mv(-1,0)->sumover
           +$T_all(:,:,0:$n)->mv(-1,0)->sumover;
    }

Con estos pedazos podemos armar un primer programa que calcula y
reporta las interacciones para una película.

    # name: interactions.pl
    <<init>>
    <<usage>>
    <<cinner>>
    <<trunc>>
    <<parameters>>
    <<area>>
    <<reciprocal>>
    <<reciprocal-decay>>
    <<T+->>
    <<interactions>>
    <<selfinteraction>>
    <<interactions-film>>
    <<missing>>
    my @dir=qw(xx yy zz);
    say "Diagonal components of the interaction";
    say "$dir[$_]: ", trunc $digits, $T_nm->(($_),($_)) for (0..2);
    say "Missing terms due to surface";
    say "$dir[$_]: ", trunc $digits,$M_n->(($_),($_)) for (0..2);

Podemos correrlo como a continuación para la superficie <img src="/assets/ltximg/2021-05-29-campolocal_c162e63ae0c9857ff94bff3b1c6ed7b003976c83.png" alt="2021-05-29-campolocal_c162e63ae0c9857ff94bff3b1c6ed7b003976c83.png" /> de
una red cúbica <img src="/assets/ltximg/2021-05-29-campolocal_6d2f2452b6b0c9fbf736df4a2202961865277da8.png" alt="2021-05-29-campolocal_6d2f2452b6b0c9fbf736df4a2202961865277da8.png" /> <img src="/assets/ltximg/2021-05-29-campolocal_d7f4549512946843b8b14078e293ac807ac5b603.png" alt="2021-05-29-campolocal_d7f4549512946843b8b14078e293ac807ac5b603.png" />, <img src="/assets/ltximg/2021-05-29-campolocal_8d2188a28131a0218b0c142da84f2afe9a3e9f80.png" alt="2021-05-29-campolocal_8d2188a28131a0218b0c142da84f2afe9a3e9f80.png" />, truncando
la red recíproca en <img src="/assets/ltximg/2021-05-29-campolocal_c3c17d7640627bd2d39a2b8d4a75777d856bb963.png" alt="2021-05-29-campolocal_c3c17d7640627bd2d39a2b8d4a75777d856bb963.png" />, permitiendo interacciones con
segundos vecinos y en una película de semiancho 3 (ancho 7):

    ./interactions.pl -a 1,0 -b 0,1 -c 0,0,1 -pqmax 2 -dmax 2 -N 3 -digits 4

Resultados:

    Diagonal components of the interaction
    xx:
    [
      [  4.5168  -0.1637  -0.0002  0  0  0  0]
      [  -0.1637  4.5168  -0.1637  -0.0002  0  0  0]
      [-0.0002  -0.1637  4.5168  -0.1637  -0.0002  0  0]
      [  0  -0.0002  -0.1637  4.5168  -0.1637  -0.0002  0]
      [  0  0  -0.0002  -0.1637  4.5168  -0.1637  -0.0002]
      [  0  0  0  -0.0002  -0.1637  4.5168  -0.1637]
      [  0  0  0  0  -0.0002  -0.1637  4.5168]
    ]

    yy:
    [
      [  4.5168  -0.1637  -0.0002  0  0  0  0]
      [  -0.1637  4.5168  -0.1637  -0.0002  0  0  0]
      [-0.0002  -0.1637  4.5168  -0.1637  -0.0002  0  0]
      [  0  -0.0002  -0.1637  4.5168  -0.1637  -0.0002  0]
      [  0  0  -0.0002  -0.1637  4.5168  -0.1637  -0.0002]
      [  0  0  0  -0.0002  -0.1637  4.5168  -0.1637]
      [  0  0  0  0  -0.0002  -0.1637  4.5168]
    ]

    zz:
    [
      [  -9.0336  0.3274  0.0005  0  0  0  0]
      [  0.3274  -9.0336  0.3274  0.0005  0  0  0]
      [0.0005  0.3274  -9.0336  0.3274  0.0005  0  0]
      [  0  0.0005  0.3274  -9.0336  0.3274  0.0005  0]
      [  0  0  0.0005  0.3274  -9.0336  0.3274  0.0005]
      [  0  0  0  0.0005  0.3274  -9.0336  0.3274]
      [  0  0  0  0  0.0005  0.3274  -9.0336]
    ]

    Missing terms due to surface
    xx: [-0.1640  -0.0002  0  0  0  -0.0002  -0.1640]
    yy: [-0.1640  -0.0002  0  0  0  -0.0002  -0.1640]
    zz: [0.3280  0.0005  0  0  0  0.0005  0.3280]

Ahora repito el cálculo pero truncando la red recíproca en <img src="/assets/ltximg/2021-05-29-campolocal_776e47fbfbb0a788652f2729d9cb4b703fd52ceb.png" alt="2021-05-29-campolocal_776e47fbfbb0a788652f2729d9cb4b703fd52ceb.png" />,

    ./interactions.pl -a 1,0 -b 0,1 -c 0,0,1 -pqmax 3 -dmax 3 -N 3 -digits 4

Resultados:

    Diagonal components of the interaction
    xx:
    [
      [  4.5168  -0.1637  -0.0002  -5.1449e-07  0  0  0]
      [  -0.1637  4.5168  -0.1637  -0.0002  -5.1449e-07  0  0]
      [-0.0002  -0.1637  4.5168  -0.1637  -0.0002  -5.1449e-07  0]
      [-5.1449e-07  -0.0002  -0.1637  4.5168  -0.1637  -0.0002  -5.1449e-07]
      [  0  -5.1449e-07  -0.0002  -0.1637  4.5168  -0.1637  -0.0002]
      [  0  0  -5.1449e-07  -0.0002  -0.1637  4.5168  -0.1637]
      [  0  0  0  -5.1449e-07  -0.0002  -0.1637  4.5168]
    ]

    yy:
    [
      [  4.5168  -0.1637  -0.0002  -5.1449e-07  0  0  0]
      [  -0.1637  4.5168  -0.1637  -0.0002  -5.1449e-07  0  0]
      [-0.0002  -0.1637  4.5168  -0.1637  -0.0002  -5.1449e-07  0]
      [-5.1449e-07  -0.0002  -0.1637  4.5168  -0.1637  -0.0002  -5.1449e-07]
      [  0  -5.1449e-07  -0.0002  -0.1637  4.5168  -0.1637  -0.0002]
      [  0  0  -5.1449e-07  -0.0002  -0.1637  4.5168  -0.1637]
      [  0  0  0  -5.1449e-07  -0.0002  -0.1637  4.5168]
    ]

    zz:
    [
      [  -9.0336  0.3274  0.0005  1.0289e-06  0  0  0]
      [  0.3274  -9.0336  0.3274  0.0005  1.0289e-06  0  0]
      [0.0005  0.3274  -9.0336  0.3274  0.0005  1.0289e-06  0]
      [1.0289e-06  0.0005  0.3274  -9.0336  0.3274  0.0005  1.0289e-06]
      [  0  1.0289e-06  0.0005  0.3274  -9.0336  0.3274  0.0005]
      [  0  0  1.0289e-06  0.0005  0.3274  -9.0336  0.3274]
      [  0  0  0  1.0289e-06  0.0005  0.3274  -9.0336]
    ]

    Missing terms due to surface
    xx: [-0.1640  -0.0002  -5.1449e-07  0  -5.1449e-07  -0.0002  -0.1640]
    yy: [-0.1640  -0.0002  -5.1449e-07  0  -5.1449e-07  -0.0002  -0.1640]
    zz: [0.3280  0.0005  1.0289e-06  0  1.0289e-06  0.0005  0.3280]

Comparando con los resultados previos, vemos que hay convergencia en
la quinta cifra. Para otras orientaciones y otras redes podría
requerirse el uso de más vectores recíprocos, pero siempre es un
número muy modesto.


# Polarización superficial

Con esto, ya podemos calcular las modificaciones superficiales a la
polarización. Para esto, modificamos nuestra lista de parámetros para
poder dar una respuesta dieléctrica y elegir una orientación.

    # name: parameters2
    my ($a,$b); # 2D basis.
    my $c;  # 3D Separation between sites in nearby planes
    my $pqmax;   # index of largest reciprocal vector
    my $dmax;   # index of largest distance to calculate
    my $N; # seminumber of planes of film
    my $direction; # cartesian direction, x y or z
    my $epsilon; # dielectric function
    my $digits=7; # number of decimal digits to print
    my $options=q(
        'a=s'=>\$a, # 2D basis vector x,y
        'b=s'=>\$b, # 2D basis vector x,y
        'c=s'=>\$c, # 3D separation x,y,z
        'pqmax=i'=>\$pqmax,  # index of largest reciprocal vector
        'dmax=i'=>\$dmax,  # index of largest distance to calculate
        'N=i'=>\$N, # seminumber of planes of film
        'dir=s'=>\$direction, # cartesian direction, x y or z
        'epsilon=s'=>\$epsilon, # dielectric function e',e''
        'digits=i'=>\$digits, # number of decimal digits to print
        );
    my %options=(eval $options);
    die "Bad option definition: $@" if $@;
    GetOptions(%options) or usage $options, "Bad options";
    usage $options, "Undefined parameters"
          unless lu_all {defined $_}
                        ($a, $b, $c, $pqmax, $dmax, $N, $direction, $epsilon);
    usage $options, "Vectors should be comma separated list of numbers"
          unless lu_all {looks_like_number $_} map {split ','} ($a, $b, $c);
    #convert from strings to vectors
    ($a,$b,$c) = map {pdl(split ',', $_)} ($a, $b, $c);
    usage $options, "Basis vectors should be 2D"
          unless lu_all {$_->dims==1 and $_->dim(0)==2} ($a, $b);
    usage $options, "c should be 3D" unless $c->dims==1 and $c->dim(0)==3;
    usage $options, "Third component of c should be positive"
          unless $c->((2)) > 0;
    usage $options, "pqmax should be positive" unless $pqmax > 0;
    usage $options, "dmax should be positive" unless $dmax > 0;
    usage $options, "dir should be x, y or z"
          unless $direction=~m{^[xyzXYZ]$};
    my %index_from_direction=(x=>0, y=>1, z=>2);
    my $dir_i=$index_from_direction{lc $direction};
    usage $options, "N should be positive" unless $N > 0;
    usage $options, "epsilon should be two comma separated numbers eps', eps''"
        unless lu_all {looks_like_number $_} split ',', $epsilon;
    $epsilon=[split ',', $epsilon];
    $epsilon=$epsilon->[0]+i()*$epsilon->[1];

Dado un campo externo normalizado <img src="/assets/ltximg/2021-05-29-campolocal_90b8a0be4f8ca4e4b9d44ef4428295f150c3b47b.png" alt="2021-05-29-campolocal_90b8a0be4f8ca4e4b9d44ef4428295f150c3b47b.png" />, podemos obtener la polarización de
bulto <img src="/assets/ltximg/2021-05-29-campolocal_e23739c5facc027eade581f1bef4088f7cd35ba2.png" alt="2021-05-29-campolocal_e23739c5facc027eade581f1bef4088f7cd35ba2.png" /> y el dipolo de bulto <img src="/assets/ltximg/2021-05-29-campolocal_1addb66d77e970b73764791d293ba804f49617c7.png" alt="2021-05-29-campolocal_1addb66d77e970b73764791d293ba804f49617c7.png" />.

    # name: pB
    my $PB=$dir_i==2?(1-1/$epsilon)/(4*PI):($epsilon-1)/(4*PI);
    my $pB=$PB/$density; # dipole moment

Usando Claussius Mossoti <img src="/assets/ltximg/2021-05-29-campolocal_fac252c9ea8aa1fcadc815fdf26d978924c51d60.png" alt="2021-05-29-campolocal_fac252c9ea8aa1fcadc815fdf26d978924c51d60.png" />
también podemos obtener la polarizabilidad <img src="/assets/ltximg/2021-05-29-campolocal_f06f20dee81ab8248628631211abcbe3c7ee9a80.png" alt="2021-05-29-campolocal_f06f20dee81ab8248628631211abcbe3c7ee9a80.png" />,

    # name: alpha
    my $alpha=3/(4*PI*$density)*($epsilon-1)/($epsilon+2);

La ecuación a resolver es


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_700610c1cd5c0789450f666d55eaeaa908deb63c.png" alt="2021-05-29-campolocal_700610c1cd5c0789450f666d55eaeaa908deb63c.png" />
</span>
<span class="equation-label">
17
</span>
</div>

La ecuación en el bulto es


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_fe1b7c231673297cccce9206154197c15baba6b5.png" alt="2021-05-29-campolocal_fe1b7c231673297cccce9206154197c15baba6b5.png" />
</span>
<span class="equation-label">
18
</span>
</div>

Restando,


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_b1d42c81ee7003c3689744a8bea62719297f57cb.png" alt="2021-05-29-campolocal_b1d42c81ee7003c3689744a8bea62719297f57cb.png" />
</span>
<span class="equation-label">
19
</span>
</div>

que reescribimos como


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_0fadeaed90d83a71672de42eeaf174427b046ce5.png" alt="2021-05-29-campolocal_0fadeaed90d83a71672de42eeaf174427b046ce5.png" />
</span>
<span class="equation-label">
20
</span>
</div>

donde <img src="/assets/ltximg/2021-05-29-campolocal_4d69e3c7fc7aadedec0c9c7c5e85b46ac2e04794.png" alt="2021-05-29-campolocal_4d69e3c7fc7aadedec0c9c7c5e85b46ac2e04794.png" /> es el tensor identidad y <img src="/assets/ltximg/2021-05-29-campolocal_0597d6bc8b8c89513b81b211b51655da1aebfb48.png" alt="2021-05-29-campolocal_0597d6bc8b8c89513b81b211b51655da1aebfb48.png" /> es la suma de las interacciones con
los planos ausentes.

Construimos entonces rutinas para resolver sistemas lineales de
ecuaciones complejas, basadas en rutinas estandard reales. Hacemos una
descomposición LU y la usamos para resolver la ecuación.

    # name: lu
    sub solve {
        my ($Matrix, $rhs)=@_;
        #Convert complex equation to real equation
        my ($Mr, $Mi)=($Matrix->re, $Matrix->im);
        my $N=$Mr->dim(0);
        my $real_M=pdl($Mr,-$Mi, $Mi, $Mr)->reshape($N,$N,2,2)
                   ->mv(2,1)->reshape(2*$N,2*$N); #assumed no extra dims.
        my $real_rhs=append($rhs->re, $rhs->im)->dummy(1); #make row vector
        my ($lu,$perm,$par) = $real_M->copy->lu_decomp;
        my $real_sol=lu_backsub($lu, $perm, $real_rhs->copy); #returns row
        my $sol=$real_sol->(0:$N-1,(0))+i()*$real_sol->($N:2*$N-1,(0));
        $sol; #ordinary complex vector
    }

Finalmente, usamos estas rutinas para resolver el sistema lineal de ecuaciones.

    # name: Dp
    my $identity=$T_nm->(($dir_i),($dir_i))->zeroes;
    $identity->diagonal(0,1)++;
    my $Dp=solve($identity-$alpha*$T_nm->(($dir_i),($dir_i)),
                 -$alpha*$M_n->(($dir_i),($dir_i))*$pB);

Armamos el programa juntando los fragmentos,

    # name Delta p
    <<init>>
    <<usage>>
    <<cinner>>
    <<trunc>>
    <<lu>>
    <<parameters2>>
    <<area>>
    <<reciprocal>>
    <<reciprocal-decay>>
    <<T+->>
    <<interactions>>
    <<selfinteraction>>
    <<interactions-film>>
    <<missing>>
    <<pB>>
    <<alpha>>
    <<Dp>>
    say trunc $digits, $Dp;

Probémoslo con un dieléctrico no disipativo.

    ./Delta_p.pl -a 1,0 -b 0,1 -c 0,0,1 -pqmax 2 -dmax 2 -N 5 -dir x \
                 -epsilon 2,0  -digits 4

Resultados:

    [0.0010  -1.2466e-05  1.4262e-07  -1.6256e-09  1.8520e-11  -4.2182e-13
      1.8520e-11  -1.6256e-09  1.4262e-07  -1.2466e-05  0.0010]

Ahora, con vacío + disipación

    ./Delta_p.pl -a 1,0 -b 0,1 -c 0,0,1 -pqmax 2 -dmax 2 -N 5 -dir x \
                 -epsilon 1,1 -digits 4

Resultados:

    [-0.0010-2.7054e-05i  -2.4601e-06+1.3453e-05i  1.7311e-07+5.9471e-08i
      1.1283e-09-2.1714e-09i  -2.6469e-11-1.9207e-11i  -6.1268e-13+6.2393e-13i
     -2.6469e-11-1.9207e-11i  1.1283e-09-2.1714e-09i  1.7311e-07+5.9471e-08i
     -2.4601e-06+1.3453e-05i  -0.0010-2.7054e-05i]


# Sistema semiinfinito.

Podemos simular un sistema semiinfinito como una película finita,
suficientemente ancha y eliminando el término que fuerza al sistema
por uno de los lados, i.e. redefiniendo las <img src="/assets/ltximg/2021-05-29-campolocal_bc9e44f15f9feac91c07f92e4f4ddeae69ba824b.png" alt="2021-05-29-campolocal_bc9e44f15f9feac91c07f92e4f4ddeae69ba824b.png" />'s. Para ello,
modificamos el bloque `missing`.

    # name: missing1
      my $M_n=zeroes(cdouble,3,3,$N2);
      for my $n(0..$N2-1){
          $M_n->(:,:,($n)).=
              $T_all->(:,:,$N2+$n+1:2*$N2)->mv(-1,0)->sumover;
      }

Con esto armamos un nuevo programa.

    # name Delta p1
    <<init>>
    <<usage>>
    <<cinner>>
    <<trunc>>
    <<lu>>
    <<parameters2>>
    <<area>>
    <<reciprocal>>
    <<reciprocal-decay>>
    <<T+->>
    <<interactions>>
    <<selfinteraction>>
    <<interactions-film>>
    <<missing1>>
    <<pB>>
    <<alpha>>
    <<Dp>>
    say trunc $digits, $Dp;

Le aplicamos las mismas pruebas que arriba.

    ./Delta_p1.pl -a 1,0 -b 0,1 -c 0,0,1 -pqmax 2 -dmax 2 -N 5 -dir x \
                  -epsilon 2,0 -digits 4

Resultados:

    [0.0010  -1.2466e-05  1.4262e-07  -1.6256e-09  1.8517e-11  -2.1091e-13
      2.4021e-15  -2.7358e-17  3.1159e-19  -3.5489e-21  4.0413e-23]

    ./Delta_p1.pl -a 1,0 -b 0,1 -c 0,0,1 -pqmax 2 -dmax 2 -N 5 -dir x \
                  -epsilon 1,1 -digits 4

Resultados:

    [-0.0010-2.7054e-05i  -2.4601e-06+1.3453e-05i  1.7311e-07+5.9471e-08i
      1.1283e-09-2.1714e-09i  -2.6473e-11-1.9211e-11i  -3.0634e-13+3.1196e-13i
     3.5181e-15+4.6669e-15i  6.8655e-17-3.7276e-17i  -3.5698e-19-9.8135e-19i
     -1.3679e-20+2.7779e-21i  9.6595e-24+1.8636e-22i]

Comparando con los resultados de la sección anterior vemos que <img src="/assets/ltximg/2021-05-29-campolocal_799cd15f1656e0fd43a0dccbc73db4a4c04536f4.png" alt="2021-05-29-campolocal_799cd15f1656e0fd43a0dccbc73db4a4c04536f4.png" /> es esencialmente idéntica al caso anterior cerca de la superficie
mientras que ahora se hace prácticamente cero en el otro extremo.


# Respuesta superficial

Ahora podemos promediar el exceso de polarización sobre la celda unitaria e
integrarla sobre la coordenada normal para obtener la corriente superficial


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_3335b75cdc8504ce4a02a8ea1b75099e00d5de8f.png" alt="2021-05-29-campolocal_3335b75cdc8504ce4a02a8ea1b75099e00d5de8f.png" />
</span>
<span class="equation-label">
21
</span>
</div>

De aquí podemos identificar las conductividades superficiales,


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_322c5a77ff60691a769d70888ab3b52712b25941.png" alt="2021-05-29-campolocal_322c5a77ff60691a769d70888ab3b52712b25941.png" />
</span>
<span class="equation-label">
22
</span>
</div>

donde <img src="/assets/ltximg/2021-05-29-campolocal_e3e2119223514d0d4138267860fe21ec674b7336.png" alt="2021-05-29-campolocal_e3e2119223514d0d4138267860fe21ec674b7336.png" /> es el área de la celda unitaria 2D, supusimos que <img src="/assets/ltximg/2021-05-29-campolocal_3773bfa0a05421f0f67e6c4791a370dbe60310e2.png" alt="2021-05-29-campolocal_3773bfa0a05421f0f67e6c4791a370dbe60310e2.png" />, <img src="/assets/ltximg/2021-05-29-campolocal_f4b063b0f80936b36f97c50c99cf1c25baca9522.png" alt="2021-05-29-campolocal_f4b063b0f80936b36f97c50c99cf1c25baca9522.png" />,
y <img src="/assets/ltximg/2021-05-29-campolocal_87596482ce53325ca7d4bd470c6fbdc163cfb5a7.png" alt="2021-05-29-campolocal_87596482ce53325ca7d4bd470c6fbdc163cfb5a7.png" /> son direcciones principales y que
usamos campos normalizados <img src="/assets/ltximg/2021-05-29-campolocal_dff68935dd7e9b7d6e39f2f30ae20e9722dd3c20.png" alt="2021-05-29-campolocal_dff68935dd7e9b7d6e39f2f30ae20e9722dd3c20.png" /> al calcular <img src="/assets/ltximg/2021-05-29-campolocal_fa2a79987f9a91227a256913eec3a47b1286cfc6.png" alt="2021-05-29-campolocal_fa2a79987f9a91227a256913eec3a47b1286cfc6.png" />, <img src="/assets/ltximg/2021-05-29-campolocal_30d30c5245f75068c1a3a860668cb991e8e0e2f3.png" alt="2021-05-29-campolocal_30d30c5245f75068c1a3a860668cb991e8e0e2f3.png" /> y <img src="/assets/ltximg/2021-05-29-campolocal_4c7eb214ae3332e786abd258b68044a0088542cb.png" alt="2021-05-29-campolocal_4c7eb214ae3332e786abd258b68044a0088542cb.png" /> al
calcular <img src="/assets/ltximg/2021-05-29-campolocal_71e297507b17ef187af348399ff6cfe05af96bc4.png" alt="2021-05-29-campolocal_71e297507b17ef187af348399ff6cfe05af96bc4.png" />.

Con estas funciones respuesta puedo calcular la impedancia superficial


<div class="equation-container">
<span class="equation">
<img src="/assets/ltximg/2021-05-29-campolocal_f64aece58acbb4b244f4839e6a0d039540da472e.png" alt="2021-05-29-campolocal_f64aece58acbb4b244f4839e6a0d039540da472e.png" />
</span>
<span class="equation-label">
23
</span>
</div>

donde elegimos las componentes apropiadas de acuerdo a la polarización
y a la orientación del plano de incidencia.

Por motivos prácticos tenemos que enfrentar ahora el problema de las
unidades. En general, <img src="/assets/ltximg/2021-05-29-campolocal_8237629ff8785539d95b194f27238b933fd653b7.png" alt="2021-05-29-campolocal_8237629ff8785539d95b194f27238b933fd653b7.png" />, <img src="/assets/ltximg/2021-05-29-campolocal_957098270886006faff7713e120e0879830fd5d8.png" alt="2021-05-29-campolocal_957098270886006faff7713e120e0879830fd5d8.png" />, por
lo que <img src="/assets/ltximg/2021-05-29-campolocal_7a7e697407ae91cca245459b75981a223e084306.png" alt="2021-05-29-campolocal_7a7e697407ae91cca245459b75981a223e084306.png" /> y los cocientes <img src="/assets/ltximg/2021-05-29-campolocal_bc902c0e08d4f39a61f6c95eed8a3cc6d650ac4a.png" alt="2021-05-29-campolocal_bc902c0e08d4f39a61f6c95eed8a3cc6d650ac4a.png" /> y <img src="/assets/ltximg/2021-05-29-campolocal_55cf24c82d8a48bf9146cdb50fed8dd3a082c55a.png" alt="2021-05-29-campolocal_55cf24c82d8a48bf9146cdb50fed8dd3a082c55a.png" /> son adimensionales. Al normalizar los campos a 1 y desproveerlos de unidades,
los dipolos calculados arriba tendrían unidades de volumen en lugar de
carga por distancia, puesto que la polarizabilidad tiene unidades de
volumen. Al dividirlos entre <img src="/assets/ltximg/2021-05-29-campolocal_e3e2119223514d0d4138267860fe21ec674b7336.png" alt="2021-05-29-campolocal_e3e2119223514d0d4138267860fe21ec674b7336.png" /> adquirirían unidades de distancia y
al multiplicarlos por <img src="/assets/ltximg/2021-05-29-campolocal_47665ddaf780ff3b93724a9966a2b5d6446e4b29.png" alt="2021-05-29-campolocal_47665ddaf780ff3b93724a9966a2b5d6446e4b29.png" /> llegaríamos a las esperadas unidades de
velocidad. Es común expresar la frecuencia en términos de la energía
<img src="/assets/ltximg/2021-05-29-campolocal_e0a3e7f12bfd0e1e3fd3153a804368fcb3c5f432.png" alt="2021-05-29-campolocal_e0a3e7f12bfd0e1e3fd3153a804368fcb3c5f432.png" /> en unidades de <img src="/assets/ltximg/2021-05-29-campolocal_29a649f7983cf2f1e7174d800a2246ef93821b3a.png" alt="2021-05-29-campolocal_29a649f7983cf2f1e7174d800a2246ef93821b3a.png" />. Por otro lado, es cómodo expresar
los vectores de la base cristalina <img src="/assets/ltximg/2021-05-29-campolocal_18db92b491aa38a76845ef1a8d75ec424e2ebac8.png" alt="2021-05-29-campolocal_18db92b491aa38a76845ef1a8d75ec424e2ebac8.png" />, <img src="/assets/ltximg/2021-05-29-campolocal_2232f20fda36a594bf6244c3a1a10bf98dfed070.png" alt="2021-05-29-campolocal_2232f20fda36a594bf6244c3a1a10bf98dfed070.png" /> y <img src="/assets/ltximg/2021-05-29-campolocal_431928413284600f006cc291fd3f4f67472baf33.png" alt="2021-05-29-campolocal_431928413284600f006cc291fd3f4f67472baf33.png" /> en
unidades del parámetro de red del sistema. Entonces, la velocidad de la luz arriba
<img src="/assets/ltximg/2021-05-29-campolocal_aad7fe24284c5c445077020611cba1191ed36604.png" alt="2021-05-29-campolocal_aad7fe24284c5c445077020611cba1191ed36604.png" /> deberíamos expresarla en unidades consistentes, por ejemplo,
eV <img src="/assets/ltximg/2021-05-29-campolocal_01a0e88c6e17d6565bcfc3fa31526e776924c771.png" alt="2021-05-29-campolocal_01a0e88c6e17d6565bcfc3fa31526e776924c771.png" /> parámetro de red. Para ello usamos el factor de conversión
<img src="/assets/ltximg/2021-05-29-campolocal_7ed0958be07c5d3d5a786ae8708792a78990f88d.png" alt="2021-05-29-campolocal_7ed0958be07c5d3d5a786ae8708792a78990f88d.png" /> e leemos el parámetro de red en
nanómetros de la línea de comandos.

Modificamos entonces una vez más nuestra lista de parámetros,
añadiendo el factor de corrección, el parámetro de red y la
frecuencia, quitando una dirección específica para iterar sobre todas.

    # name: parameters3
    use constant hbar_c=>197.3; # eV nm
    my ($a,$b); # 2D basis.
    my $c;  # 3D Separation between sites in nearby planes
    my $pqmax;   # index of largest reciprocal vector
    my $dmax;   # index of largest distance to calculate
    my $N; # seminumber of planes of film
    my $epsilon; # dielectric function
    my $lattice; #lattice parameter in nm
    my $hbar_w; # frequency in eV
    my $digits=7; # number of decimal digits to print
    my $options=q(
        'a=s'=>\$a, # 2D basis vector x,y
        'b=s'=>\$b, # 2D basis vector x,y
        'c=s'=>\$c, # 3D separation x,y,z
        'pqmax=i'=>\$pqmax,  # index of largest reciprocal vector
        'dmax=i'=>\$dmax,  # index of largest distance to calculate
        'N=i'=>\$N, # seminumber of planes of film
        'epsilon=s'=>\$epsilon, # dielectric function e',e''
        'lattice=f'=>\$lattice, #lattice parameter in nm
        'frequency=f'=>\$hbar_w, # frequency in eV
        'digits=i'=>\$digits, # number of decimal digits to print
        );
    my %options=(eval $options);
    die "Bad option definition: $@" if $@;
    GetOptions(%options) or usage $options, "Bad options";
    usage $options, "Undefined parameters"
          unless lu_all {defined $_}
                        ($a, $b, $c, $pqmax, $dmax, $N, $epsilon,
                         $lattice, $hbar_w);
    usage $options, "Vectors should be comma separated list of numbers"
          unless lu_all {looks_like_number $_} map {split ','} ($a, $b, $c);
    #convert strings->vectors
    ($a,$b,$c) = map {pdl(split ',', $_)} ($a, $b, $c);
    usage $options, "Basis vectors should be 2D"
          unless lu_all {$_->dims==1 and $_->dim(0)==2} ($a, $b);
    usage $options, "c should be 3D" unless $c->dims==1 and $c->dim(0)==3;
    usage $options, "Third component of c should be positive"
        unless $c->((2)) > 0;
    usage $options, "pqmax should be positive" unless $pqmax > 0;
    usage $options, "dmax should be positive" unless $dmax > 0;
    usage $options, "N should be positive" unless $N > 0;
    usage $options,
        "epsilon should be two comma separated numbers eps', eps''"
        unless lu_all {looks_like_number $_} split ',', $epsilon;
    $epsilon=[split ',', $epsilon];
    $epsilon=$epsilon->[0]+i()*$epsilon->[1];

Ahora calculamos las tres conductividades normalizadas,

    # name: sigmas
        my @sigma= map {
        my $PB=$_==2?(1-1/$epsilon)/(4*PI):($epsilon-1)/(4*PI);
        my $pB=$PB/$density; # dipole moment
        my $identity=$T_nm->(($_),($_))->zeroes;
        $identity->diagonal(0,1)++;
        my $Dp=solve($identity-$alpha*$T_nm->(($_),($_)),
    		 -$alpha*$M_n->(($_),($_))*$pB);
        -i()*$hbar_w*$lattice*$Dp->sumover/(hbar_c*$A);
    } (0..2);

Con esto armamos un nuevo programa.

    # name sigma
    <<init>>
    <<usage>>
    <<cinner>>
    <<trunc>>
    <<lu>>
    <<parameters3>>
    <<area>>
    <<reciprocal>>
    <<reciprocal-decay>>
    <<T+->>
    <<interactions>>
    <<selfinteraction>>
    <<interactions-film>>
    <<missing1>>
    <<alpha>>
    <<sigmas>>
    my @dirs_from_index=qw(xx yy zz);
    say "$dirs_from_index[$_]: $sigma[$_]" for (0..2);

Ahora lo corremos para un aislante en una red cúbica simple.

    ./sigma.pl -a 1,0 -b 0,1 -c 0,0,1 -pqmax 2 -dmax 2\
                -N 5 -epsilon 2,0 -lattice .4 -frequency 10 -digits 4

Resultados:

    xx: -2.13738209040293e-05i
    yy: -2.13738209040293e-05i
    zz: 1.04118689039735e-05i


# Reflectancia diferencial

Tenemos ya prácticamente todas las herramientas para calcular los
cambios en la reflectancia. Para ello, en lugar de leer un valor de
<img src="/assets/ltximg/2021-05-29-campolocal_864c1b06476ce85912aae4acfd7a12387ec732ce.png" alt="2021-05-29-campolocal_864c1b06476ce85912aae4acfd7a12387ec732ce.png" /> desde la línea de comandos, leeremos el nombre de un
archivo con una tabla de valores de frecuencia, <img src="/assets/ltximg/2021-05-29-campolocal_e2954ff64cd56284c636605f81662d6bfaa549f2.png" alt="2021-05-29-campolocal_e2954ff64cd56284c636605f81662d6bfaa549f2.png" /> y
<img src="/assets/ltximg/2021-05-29-campolocal_8f97d65305fce68d9848ae098d84cd1dc04f44c0.png" alt="2021-05-29-campolocal_8f97d65305fce68d9848ae098d84cd1dc04f44c0.png" /> para, y para cada valor obtendremos la impedancia
superficial, la conductividad superficial y la reflectancia. A la
lista de parámetros hay que añadir el nombre del archivo, el ángulo
de incidencia y el nombre del archivo de salida.

    # name: parameters4
    use constant hbar_c=>197.3; # eV nm
    my ($a,$b); # 2D basis.
    my $c;  # 3D Separation between sites in nearby planes
    my $pqmax;   # index of largest reciprocal vector
    my $dmax;   # index of largest distance to calculate
    my $N; # seminumber of planes of film
    my $lattice; #lattice parameter in nm
    my $angle; #incidence angle (degrees)
    my $ifilename;  # name of input file: hnu eps' eps''
    my $title;  # title of the output plot
    my $ofilename;  # name of output plot (png)
    my $digits=7; # number of decimal digits to print
    my $options=q(
    	'a=s'=>\$a, # 2D basis vector x,y
          	'b=s'=>\$b, # 2D basis vector x,y
          	'c=s'=>\$c, # 3D separation x,y,z
          	'pqmax=i'=>\$pqmax,  # index of largest reciprocal vector
          	'dmax=i'=>\$dmax,  # index of largest distance to calculate
          	'N=i'=>\$N, # seminumber of planes of film
          	'lattice=f'=>\$lattice, #lattice parameter in nm
    	'angle=f'=>\$angle, #incidence angle (degrees)
          	'ifilename=s'=>\$ifilename, # name of input file: hnu eps' eps''
    	'ofilename=s'=>\$ofilename, # name of output plot (png)
            'title=s'=>\$title,  # title of the output plot
          	'digits=i'=>\$digits, # number of decimal digits to print
          );
    my %options=(eval $options);
    die "Bad option definition: $@" if $@;
    GetOptions(%options) or usage $options, "Bad options";
    usage $options, "Undefined parameters"
        unless lu_all {defined $_}
    ($a, $b, $c, $pqmax, $dmax, $N, $lattice, $angle, $ifilename,
         $ofilename, $title);
    usage $options, "Vectors should be comma separated list of numbers"
        unless lu_all {looks_like_number $_} map {split ','} ($a, $b, $c);
    #convert strings->vectors
    ($a,$b,$c) = map {pdl(split ',', $_)} ($a, $b, $c);
    usage $options, "Basis vectors should be 2D"
        unless lu_all {$_->dims==1 and $_->dim(0)==2} ($a, $b);
    usage $options, "c should be 3D" unless $c->dims==1 and $c->dim(0)==3;
    usage $options, "Third component of c should be positive"
        unless $c->((2)) > 0;
    usage $options, "pqmax should be positive" unless $pqmax > 0;
    usage $options, "dmax should be positive" unless $dmax > 0;
    usage $options, "N should be positive" unless $N > 0;
    usage $options, "Angle should be between 0 and 90"
        unless $angle >=0 and $angle < 90;
    my $angler=$angle*PI/180; # angle in radians
    usage $options, "ifilename should be readable" unless -r $ifilename;
    # frequency in eV, real, imag and full dielectric function
    my ($hbar_ws, $epsilons1, $epsilons2)=rcols $ifilename;
    usage $options,
        "File should have three columns of space separated numbers"
        unless $hbar_ws->dim(0)==$epsilons1->dim(0) and
        $hbar_ws->dim(0)==$epsilons2->dim(0) and  $hbar_ws->dim(0) > 0;
    my $epsilons=$epsilons1+i()*$epsilons2;

Aprovechando que en `PDL`, rutinas diseñadas para actuar sobre un
escalar se pueden aplicar a arreglos multidimensionales sin
modificación, entonces el fragmento `alpha` puede ser usado sin
modificación. Sin embargo, los fragmentos `lu` y `sigma` si deben modificarse
para acomodar la nueva dimensión (la frecuencia). Aunque no es lo más
elegante, podemos evitarlo y reciclar los fragmentos previos si
hacemos una iteración. Una solución más elegante hubiera sido preveer
el reciclar cada fragmento construyéndolo como módulos a usar o como
subrutinas con argumentos en lugar de ser fragmentos a incorporar en un *código*
lineal (de *espageti*) y comunicarnos mediante el nombre de las
variables. Es el precio a pagar por armar el código
incrementalmente. Dentro cada iteración podemos también calculamos la
impedancia superficial y la reflectancia.

Primero calculo la impedancia superficial no perturbada, la impedancia
perturbada, la amplitud de reflexión y la reflectancia.

    # name DR/R
    my $q=1+0*i(); # normalize to free wavevector
    my $Q=$q*sin($angler);
    my ($kv, $km)= map {mysqrt($_*$q**2-$Q**2)} (1, $epsilon);
    my ($Zsv, $Zpv)= ($q/$kv, $kv/$q);
    my ($Zsm0, $Zpm0)= ($q/$km, $km/($q*$epsilon));
    my @Zsm=map {$Zsm0/(1+4*PI*$Zsm0*$_)} @sigma[0,1];
    my @Zpm=map {($Zpm0+4*PI*$Q**2/$q**2*$sigma[2])/(1+4*PI*$Zpm0*$_)}
                @sigma[0,1];
    #perturbed and non perturbed
    my ($rs0,@rs)=map {($_-$Zsv)/($_+$Zsv)} $Zsm0, @Zsm;
    my ($rp0,@rp)=map {($Zpv-$_)/($Zpv+$_)} $Zpm0, @Zpm;
    my ($Rs0,@Rs)=map {$_->abs**2} ($rs0,@rs);
    my ($Rp0,@Rp)=map {$_->abs**2} ($rp0,@rp);
    my @DRRs=map {($Rs[$_]-$Rs0)/$Rs0} (0,1); #differential
    my @DRRp=map {($Rp[$_]-$Rp0)/$Rp0} (0,1);

El cálculo de la impedancia requiere una nueva rutina de utilería
`mysqrt`; como la raiz cuadrada tiene dos ramas, debo escoger aquella
con parte imaginaria no negativa, i.e., colocando el corte ramal justo
abajo del eje positivo.

    # name mysqrt
    sub mysqrt {
        my $x2=shift @_;
        my $x=sqrt($x2);
        $x=-$x if $x->im <0;
        return $x;
    }

    # name DeltaR
    <<init>>
    <<usage>>
    <<cinner>>
    <<trunc>>
    <<mysqrt>>
    <<lu>>
    <<parameters4>>
    <<area>>
    <<reciprocal>>
    <<reciprocal-decay>>
    <<T+->>
    <<interactions>>
    <<selfinteraction>>
    <<interactions-film>>
    <<missing1>>
    use PDL::Graphics::Gnuplot;
    my @results; # accumulate results
    for my $r(0..$hbar_ws->dim(0)-1){ # iterate over rows
        my $hbar_w=$hbar_ws->(($r));
        my $epsilon=$epsilons->(($r));
        <<alpha>>
        <<sigmas>>
        <<DR/R>>
        push @results, [$hbar_w, @DRRs, @DRRp];
    }
    my ($hbar_w, $DRRsx, $DRRsy, $DRRpx, $DRRpy)=
        map {my $i=$_; pdl(map {$_->[$i]} @results)} (0..4);
    my $win=gpwin("png", output=>$ofilename);
    $win->plot({title=>$title, xlabel=>'Frecuencia (eV)',
                ylabel=>'Anisotropía {/Symbol D}R/R'},
           {with=>'lines', legend=>'Pol S'}, $hbar_w, $DRRsx-$DRRsy,
           {with=>'lines', legend=>'Pol P'}, $hbar_w, $DRRpx-$DRRpy);

Ahora corremos el cálculo para la cara (110) del Si.

    ./DeltaR.pl -a .7071,0 -b 0,1 -c .3536,.5,.3536 \
         -pqmax 3 -dmax 5 -N 5 -lattice .54 -angle 0 \
         -ifilename epsSiAsp.dat -ofilename si110.png \
         -title 'Anisotropía (R_y-R_x)/R para Si (110) Incidencia normal'

Los resultados quedan en la siguiente gráfica
![img](../../../../assets/image/20210529si110.png)

Lo volvemos a correr pero ahora a un ángulo de incidencia <img src="/assets/ltximg/2021-05-29-campolocal_5375c223cddd738c43e63b905d4124f6dc0d5427.png" alt="2021-05-29-campolocal_5375c223cddd738c43e63b905d4124f6dc0d5427.png" />.

    ./DeltaR.pl -a .7071,0 -b 0,1 -c .3536,.5,.3536 \
         -pqmax 3 -dmax 5 -N 5 -lattice .54 -angle 45 \
         -ifilename epsSiAsp.dat -ofilename si110-45.png \
         -title 'Anisotropía (R_y-R_x)/R para Si (110) {/Symbol Q}_i=45'

![img](../../../../assets/image/20210529si110-45.png)

Curiosamente, aunque la respuesta normal es la misma para ambas
polarizaciones, como <img src="/assets/ltximg/2021-05-29-campolocal_58942e5c972a07841f4d98ee8b9febaba6413d8a.png" alt="2021-05-29-campolocal_58942e5c972a07841f4d98ee8b9febaba6413d8a.png" /> es menor, la anisotropía relativa es
mayor.


# Conclusiones

Partimos de una idea muy simple, el efecto de campo local no tiene por
qué ser idéntico en la vecindad de una superficie que en su
interior. Para exporar las consecuencias desarrollamos una técnica
para calcular la suma de interacciones dipolares por planos,
discutimos cómo calcular la autointeracción de cada plano, y luego
hallamos y resolvimos las ecuaciones que cumple el exceso de momento
dipolar de cada sitio por hallarse cerca de la superficie y con el
mismo, obtuvimos la conductividad superficial, la impedancia
superficial y finalmente la reflectancia. Esta resulta tener una
pequeña dependencia con la cara cristalina iluminada, y en el caso de
caras anisotrópicas, con la polarización de la luz incidente. En este
último caso, hay una anisotropía óptica inducida por la superficie en
sistemas nominalmente isotrópicos. Como esta anisotropía se produce en
las primeras camadas atómicas, su valor y la estructura de sus
espectros dependen fuertemente de la condición de la superficie, y es
fuertemente modificada por la presencia de adsorbatos, por la
relajación y la reconstrucción superficial, por los cambios a la
estructura electrónica, por la presencia de estados de superficie, por
su modulación mediante campos externos y por los cambios de
composición química. Esto permite que la espectroscopía de anisotropía
en la reflectancia, conocida como RAS, sea empleada como una
herramienta para *observar* superficies tanto dentro como fuera de
cámaras de ultra-alto vacío, e incluso en ambientes químicamente
hostiles. RAS se ha convertido en una espectroscopía óptica empleada
rutinariamente en la industria semiconductora para monitorear la
cinemática y para entender la dinámica del crecimiento epitaxial, así
como para observar un sinnúmero de procesos superficiales.


# Notas

Para preparar estas notas usé el editor extensible *emacs* y su modo
*Org mode*, el cual permite escribir con facilidad un texto
estructurado (artículo, libro, página web), incluyendo en él
fragmentos de código computacional que pueden ensamblarse
automáticamente, correrse y desplegar sus resultados en el mismo
archivo. Los programas fueron escritos en el lenguaje `Perl` y su
extensión numérica `Perl Data Language`.
