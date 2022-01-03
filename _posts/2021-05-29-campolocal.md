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
<img src="ltximg/2021-05-29-campolocal_e2c293158c3637fe6f8e64df392e83613506a535.png" alt="2021-05-29-campolocal_e2c293158c3637fe6f8e64df392e83613506a535.png" />. Sin efecto de campo local, la respuesta dieléctrica
macroscópica sería


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_185de58eb13e007cfc23426d5e68ba94c3d24912.png" alt="2021-05-29-campolocal_185de58eb13e007cfc23426d5e68ba94c3d24912.png" />
</span>
<span class="equation-label">
1
</span>
</div>

con <img src="ltximg/2021-05-29-campolocal_25bc0c5f4dbb55398a510476e8dbed5133220340.png" alt="2021-05-29-campolocal_25bc0c5f4dbb55398a510476e8dbed5133220340.png" /> la densidad de
las entidades polarizables. Sin embargo, al tomar en cuenta que la
polarizabilidad es la respuesta no sólo al campo externo, sino también
al campo producido por todos los dipolos vecinos, la ecuación anterior
se ve reemplazada por la relación de Claussius-Mossoti,


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_02ef850eed7553198ea9e29ee43c13c10a13ddad.png" alt="2021-05-29-campolocal_02ef850eed7553198ea9e29ee43c13c10a13ddad.png" />
</span>
<span class="equation-label">
2
</span>
</div>


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_d2fda05fc40e9d22207caf89800faa5ce01bc44f.png" alt="2021-05-29-campolocal_d2fda05fc40e9d22207caf89800faa5ce01bc44f.png" />
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

Consideremos una red de Bravais bidimensional <img src="ltximg/2021-05-29-campolocal_704c1dd5632168584e984b017c06a70ccd8554ad.png" alt="2021-05-29-campolocal_704c1dd5632168584e984b017c06a70ccd8554ad.png" /> en el plano
<img src="ltximg/2021-05-29-campolocal_587a29d7c310ba623560fbfea3313a6af60d74f4.png" alt="2021-05-29-campolocal_587a29d7c310ba623560fbfea3313a6af60d74f4.png" /> ocupada por
cargas puntuales unitarias <img src="ltximg/2021-05-29-campolocal_4a295e90e977424bd9a61bc10c16590e1a29b95a.png" alt="2021-05-29-campolocal_4a295e90e977424bd9a61bc10c16590e1a29b95a.png" />. El potencial electrostático
<img src="ltximg/2021-05-29-campolocal_b0d5e0f8341d1b06b8e355f512ea369a635604d5.png" alt="2021-05-29-campolocal_b0d5e0f8341d1b06b8e355f512ea369a635604d5.png" /> que
produciría en un punto <img src="ltximg/2021-05-29-campolocal_48b6e224e8965a6f07d03a0675bff458011e2746.png" alt="2021-05-29-campolocal_48b6e224e8965a6f07d03a0675bff458011e2746.png" /> es


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_3cb1b6cf287ee938536b8fbf19fa5e0fba4db98a.png" alt="2021-05-29-campolocal_3cb1b6cf287ee938536b8fbf19fa5e0fba4db98a.png" />
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
<img src="ltximg/2021-05-29-campolocal_2fd797ac9d1757f7d973617d25734ba3669427e1.png" alt="2021-05-29-campolocal_2fd797ac9d1757f7d973617d25734ba3669427e1.png" />
</span>
<span class="equation-label">
5
</span>
</div>

en el espacio recíproco <img src="ltximg/2021-05-29-campolocal_bb07ac7f892cf16c9b711df38b56c6952159203a.png" alt="2021-05-29-campolocal_bb07ac7f892cf16c9b711df38b56c6952159203a.png" /> definido por <img src="ltximg/2021-05-29-campolocal_becc1856f40d6e5e5c940e3337c815de35afd10d.png" alt="2021-05-29-campolocal_becc1856f40d6e5e5c940e3337c815de35afd10d.png" />,


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_8c2cce7c2fa17bf8d3ea9a670bc3de0652e6cb40.png" alt="2021-05-29-campolocal_8c2cce7c2fa17bf8d3ea9a670bc3de0652e6cb40.png" />
</span>
<span class="equation-label">
6
</span>
</div>

con <img src="ltximg/2021-05-29-campolocal_fc00c730231b2880e54eb5ca170b74e7e0e879be.png" alt="2021-05-29-campolocal_fc00c730231b2880e54eb5ca170b74e7e0e879be.png" /> es el coeficiente de Fourier 2D del potencial
<img src="ltximg/2021-05-29-campolocal_b0d5e0f8341d1b06b8e355f512ea369a635604d5.png" alt="2021-05-29-campolocal_b0d5e0f8341d1b06b8e355f512ea369a635604d5.png" /> evaluado a la altura <img src="ltximg/2021-05-29-campolocal_3612876dfbe476ef94d2b3f426edd001d067800b.png" alt="2021-05-29-campolocal_3612876dfbe476ef94d2b3f426edd001d067800b.png" />.
La solución que decae al alejarnos del plano <img src="ltximg/2021-05-29-campolocal_587a29d7c310ba623560fbfea3313a6af60d74f4.png" alt="2021-05-29-campolocal_587a29d7c310ba623560fbfea3313a6af60d74f4.png" /> para <img src="ltximg/2021-05-29-campolocal_a81c575ede89abd139f128164f964cb3231bfd28.png" alt="2021-05-29-campolocal_a81c575ede89abd139f128164f964cb3231bfd28.png" /> es


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_868965c0631ad078ef61434b05bb7a39e92adceb.png" alt="2021-05-29-campolocal_868965c0631ad078ef61434b05bb7a39e92adceb.png" />
</span>
<span class="equation-label">
7
</span>
</div>

Regresando al espacio real, el potencial queda dado por


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_fd9206e932e9305e2cfa84bd4ba7877bd4d20a81.png" alt="2021-05-29-campolocal_fd9206e932e9305e2cfa84bd4ba7877bd4d20a81.png" />
</span>
<span class="equation-label">
8
</span>
</div>

donde añadimos al termino <img src="ltximg/2021-05-29-campolocal_7cde967cd01035e6fa98ac904b2648dc17982ba4.png" alt="2021-05-29-campolocal_7cde967cd01035e6fa98ac904b2648dc17982ba4.png" /> correspondiente al potencial producido
por una película uniformemente cargada, y dónde introdujimos los
vectores


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_9b9c81052f95749b13dce3686e0daffcbd0571d3.png" alt="2021-05-29-campolocal_9b9c81052f95749b13dce3686e0daffcbd0571d3.png" />
</span>
<span class="equation-label">
9
</span>
</div>

y empleamos el signo <img src="ltximg/2021-05-29-campolocal_ef2955fd00ce4f9b56df0676f4b6eaa448d3097c.png" alt="2021-05-29-campolocal_ef2955fd00ce4f9b56df0676f4b6eaa448d3097c.png" /> cuando <img src="ltximg/2021-05-29-campolocal_870a960f35d25a591f1ab39f08922b163eb7715a.png" alt="2021-05-29-campolocal_870a960f35d25a591f1ab39f08922b163eb7715a.png" /> y el signo <img src="ltximg/2021-05-29-campolocal_27ad620a0d2a5d229a29c1afead98aefbe1768ce.png" alt="2021-05-29-campolocal_27ad620a0d2a5d229a29c1afead98aefbe1768ce.png" /> cuando
<img src="ltximg/2021-05-29-campolocal_0f083b0254b9fbb7866309ff1ea45a31444bb302.png" alt="2021-05-29-campolocal_0f083b0254b9fbb7866309ff1ea45a31444bb302.png" />. Esta es una serie rápidamente convergente siempre y cuando
<img src="ltximg/2021-05-29-campolocal_94ebf9218a19eebe66222c90a1f3ac6b3f6d6c7d.png" alt="2021-05-29-campolocal_94ebf9218a19eebe66222c90a1f3ac6b3f6d6c7d.png" />.

Consideremos ahora la misma red de Bravais, pero ocupada por
dipolos idénticos <img src="ltximg/2021-05-29-campolocal_1db842fad2c838b023ea1f53882dff413c51c20e.png" alt="2021-05-29-campolocal_1db842fad2c838b023ea1f53882dff413c51c20e.png" />. La densidad de carga sería entonces


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_d32c5e14e6d42db7dc90dcfd458c1fba21608529.png" alt="2021-05-29-campolocal_d32c5e14e6d42db7dc90dcfd458c1fba21608529.png" />
</span>
<span class="equation-label">
10
</span>
</div>

i.e., operamos sobre la densidad monopolar con el operador <img src="ltximg/2021-05-29-campolocal_e5b1f0031712fc25db5cecd710fa20757bada6cc.png" alt="2021-05-29-campolocal_e5b1f0031712fc25db5cecd710fa20757bada6cc.png" />. Luego,
el potencial dipolar <img src="ltximg/2021-05-29-campolocal_11290640cdf3f1b3255efced424d68d9734e1b80.png" alt="2021-05-29-campolocal_11290640cdf3f1b3255efced424d68d9734e1b80.png" /> se obtiene aplicando el mismo
operador sobre el potencial monopolar, <img src="ltximg/2021-05-29-campolocal_32edb2c7b21d92791f4fc6dc1d6b8bf6636aee51.png" alt="2021-05-29-campolocal_32edb2c7b21d92791f4fc6dc1d6b8bf6636aee51.png" />,


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_ed275a6ebc1beb4ccce37426e74f065633c6f39e.png" alt="2021-05-29-campolocal_ed275a6ebc1beb4ccce37426e74f065633c6f39e.png" />
</span>
<span class="equation-label">
11
</span>
</div>

y el campo eléctrico <img src="ltximg/2021-05-29-campolocal_697c13de450a55970105f106bcb2dda7335a74c3.png" alt="2021-05-29-campolocal_697c13de450a55970105f106bcb2dda7335a74c3.png" />,


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_4fed38b9429a341d83f231217a1d0300997cc08c.png" alt="2021-05-29-campolocal_4fed38b9429a341d83f231217a1d0300997cc08c.png" />
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
<img src="ltximg/2021-05-29-campolocal_ea0da930276895c49d520032bf4988dcd2c71187.png" alt="2021-05-29-campolocal_ea0da930276895c49d520032bf4988dcd2c71187.png" />
</span>
<span class="equation-label">
13
</span>
</div>

donde <img src="ltximg/2021-05-29-campolocal_bddc27b92ee3905056a424913c476e888029f111.png" alt="2021-05-29-campolocal_bddc27b92ee3905056a424913c476e888029f111.png" /> representa el campo eléctrico en el
sitio <img src="ltximg/2021-05-29-campolocal_dffc34e67b8b42cbdf0d40922d88834991f61db0.png" alt="2021-05-29-campolocal_dffc34e67b8b42cbdf0d40922d88834991f61db0.png" /> producido por un dipolo que <img src="ltximg/2021-05-29-campolocal_2c67c71625a696f975ef6b8b98d00ed9f7640b47.png" alt="2021-05-29-campolocal_2c67c71625a696f975ef6b8b98d00ed9f7640b47.png" /> en el sitio
<img src="ltximg/2021-05-29-campolocal_8fae7b1b46805761452f5e361856d70580cb5ec3.png" alt="2021-05-29-campolocal_8fae7b1b46805761452f5e361856d70580cb5ec3.png" />. Suponiendo que todos los dipolos de un plano son equivalentes,
podemos  podemos sumar las interacciones por planos
cristalinos. Definimos entonces


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_64fd91edab0083ef62d6e53e54bac48da343c6e9.png" alt="2021-05-29-campolocal_64fd91edab0083ef62d6e53e54bac48da343c6e9.png" />
</span>
<span class="equation-label">
14
</span>
</div>

donde <img src="ltximg/2021-05-29-campolocal_dffc34e67b8b42cbdf0d40922d88834991f61db0.png" alt="2021-05-29-campolocal_dffc34e67b8b42cbdf0d40922d88834991f61db0.png" /> es un sitio cualquiera del plano <img src="ltximg/2021-05-29-campolocal_25bc0c5f4dbb55398a510476e8dbed5133220340.png" alt="2021-05-29-campolocal_25bc0c5f4dbb55398a510476e8dbed5133220340.png" />. Usando el campo
dipolar previo,
la interacción entre planos cristalinos está dada por el tensor


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_59742332bafba00c7a6cb2d97f5c1b1b525a7a68.png" alt="2021-05-29-campolocal_59742332bafba00c7a6cb2d97f5c1b1b525a7a68.png" />
</span>
<span class="equation-label">
15
</span>
</div>

donde <img src="ltximg/2021-05-29-campolocal_8f6e718fae1e0aa83a7403ddeaa8d416a474a963.png" alt="2021-05-29-campolocal_8f6e718fae1e0aa83a7403ddeaa8d416a474a963.png" /> son vectores recíprocos bidimensionales, <img src="ltximg/2021-05-29-campolocal_f719d5849b622408ce423485031ff0992b2e9dd4.png" alt="2021-05-29-campolocal_f719d5849b622408ce423485031ff0992b2e9dd4.png" /> es
un vector que va de un sitio del plano <img src="ltximg/2021-05-29-campolocal_827aac8196c52224577029d63bc55d00f49747de.png" alt="2021-05-29-campolocal_827aac8196c52224577029d63bc55d00f49747de.png" /> a uno del plano <img src="ltximg/2021-05-29-campolocal_e551bcb3eed6d2bb41f08e6b40e53348bb5add08.png" alt="2021-05-29-campolocal_e551bcb3eed6d2bb41f08e6b40e53348bb5add08.png" />, y
donde usamos el signo <img src="ltximg/2021-05-29-campolocal_ef2955fd00ce4f9b56df0676f4b6eaa448d3097c.png" alt="2021-05-29-campolocal_ef2955fd00ce4f9b56df0676f4b6eaa448d3097c.png" /> cuando <img src="ltximg/2021-05-29-campolocal_22ef989ff080025d5f7bc21a31b0886d2e0c898b.png" alt="2021-05-29-campolocal_22ef989ff080025d5f7bc21a31b0886d2e0c898b.png" /> y el signo <img src="ltximg/2021-05-29-campolocal_27ad620a0d2a5d229a29c1afead98aefbe1768ce.png" alt="2021-05-29-campolocal_27ad620a0d2a5d229a29c1afead98aefbe1768ce.png" /> cuando <img src="ltximg/2021-05-29-campolocal_bab61c43e2bb93075b104ea626fb0226b7678dc5.png" alt="2021-05-29-campolocal_bab61c43e2bb93075b104ea626fb0226b7678dc5.png" />.
Para el caso <img src="ltximg/2021-05-29-campolocal_ed56d73b377e77de5921cc61f29aead2a977d2fc.png" alt="2021-05-29-campolocal_ed56d73b377e77de5921cc61f29aead2a977d2fc.png" /> podemos usar la regla de suma


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_a24edcf6f274d323a983658d2d4aee8edcf286bb.png" alt="2021-05-29-campolocal_a24edcf6f274d323a983658d2d4aee8edcf286bb.png" />
</span>
<span class="equation-label">
16
</span>
</div>

en el bulto del sistema, con <img src="ltximg/2021-05-29-campolocal_25bc0c5f4dbb55398a510476e8dbed5133220340.png" alt="2021-05-29-campolocal_25bc0c5f4dbb55398a510476e8dbed5133220340.png" /> la densidad de entidades
polarizables, y despejar <img src="ltximg/2021-05-29-campolocal_576fb66b122a509b66e98253e69044b4c607308c.png" alt="2021-05-29-campolocal_576fb66b122a509b66e98253e69044b4c607308c.png" /> (sin suma), la autointeracción
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

Calcula el área de la celda unitaria 2D <img src="ltximg/2021-05-29-campolocal_7e7c85cc5ceb310502ceb36c62513e51f29e5794.png" alt="2021-05-29-campolocal_7e7c85cc5ceb310502ceb36c62513e51f29e5794.png" />, el volumen de la celda
unitaria 3D <img src="ltximg/2021-05-29-campolocal_c63faddebdfc03981ec1914c347cfbac8cae0794.png" alt="2021-05-29-campolocal_c63faddebdfc03981ec1914c347cfbac8cae0794.png" /> y la densidad

    # name: area
    my $A=($a->((0))*$b->((1))-$a->((1))*$b->((0)))->abs;
    my $V=$A*$c->((2));
    my $density=1/$V;

Genera la red recíproca <img src="ltximg/2021-05-29-campolocal_fb9030a975bb06fcb40f57328479db5a26f217f5.png" alt="2021-05-29-campolocal_fb9030a975bb06fcb40f57328479db5a26f217f5.png" />, donde
<img src="ltximg/2021-05-29-campolocal_3b26a342f6c18306e1ea9e97cbb18de91f3063b0.png" alt="2021-05-29-campolocal_3b26a342f6c18306e1ea9e97cbb18de91f3063b0.png" /> son los elementos de la base dual,
<img src="ltximg/2021-05-29-campolocal_d48ee67dcc50e0a00739c1926c0872a4b61ba8a9.png" alt="2021-05-29-campolocal_d48ee67dcc50e0a00739c1926c0872a4b61ba8a9.png" />. En 2D,
<img src="ltximg/2021-05-29-campolocal_52fcd57b728f0f179e5210d0f6a60a78a9533090.png" alt="2021-05-29-campolocal_52fcd57b728f0f179e5210d0f6a60a78a9533090.png" /> y
<img src="ltximg/2021-05-29-campolocal_d239b825d8f5a3f7a5e597e0830452985fda2142.png" alt="2021-05-29-campolocal_d239b825d8f5a3f7a5e597e0830452985fda2142.png" />. En el programa
uso `$a` y `$b` para denotar la base y `$Ga$ y ~$Gb` para la base
dual.

    # name: reciprocal
    my ($a_perp, $b_perp)=map {pdl(-$_->((1)), $_->((0)))} ($a, $b);
    my ($Ga, $Gb)=map {2*PI*$_->[0]/inner($_->[0], $_->[1])}
    		  ([$b_perp, $a], [$a_perp, $b]);
    my $pq=zeroes(2*$pqmax+1,2*$pqmax+1)->ndcoords-$pqmax; #i,p,q
    my $G=$pq->((0),*1)*$Ga+$pq->((1),*1)*$Gb;  #i,p,q

Genera los vectores 3D <img src="ltximg/2021-05-29-campolocal_49b0535496702a2ba95c94e6c263113246e108da.png" alt="2021-05-29-campolocal_49b0535496702a2ba95c94e6c263113246e108da.png" />.

    # name: reciprocal-decay
    my $G_abs=inner($G, $G)->sqrt; # p,q
    my ($g_p, $g_m)=map {append($G, ($_*i()*$G_abs)->(*1))} (+1,-1); # i,p,q

Con ellos arma los tensores <img src="ltximg/2021-05-29-campolocal_e63f15d72c43e1d5c6babd2d33dc1515ba4000bb.png" alt="2021-05-29-campolocal_e63f15d72c43e1d5c6babd2d33dc1515ba4000bb.png" />.

    # name: T+-
    # i,j,gx,gy
    my ($T_p, $T_m)= map {-2*PI/$A*$_->(*1,:)*$_->(:,*1)/$G_abs->(*1,*1)}
    		     ($g_p, $g_m); # i,j,p,q
    $_->(:,:,$pqmax,$pqmax).=0 foreach ($T_p, $T_m); # Fix division by 0

Ahora arma las interacciones <img src="ltximg/2021-05-29-campolocal_6b93e966c5d37195f6333284f4552e8567bbacc0.png" alt="2021-05-29-campolocal_6b93e966c5d37195f6333284f4552e8567bbacc0.png" /> para <img src="ltximg/2021-05-29-campolocal_25bc0c5f4dbb55398a510476e8dbed5133220340.png" alt="2021-05-29-campolocal_25bc0c5f4dbb55398a510476e8dbed5133220340.png" /> positiva y negativa.

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

Arma las interacciones <img src="ltximg/2021-05-29-campolocal_a0a6326ca65e5eb01efbc13fdc49bfc66cd73e64.png" alt="2021-05-29-campolocal_a0a6326ca65e5eb01efbc13fdc49bfc66cd73e64.png" /> por bloques para una película
con <img src="ltximg/2021-05-29-campolocal_7402810b6f48472876bc851c11b76b5d9c9a58b8.png" alt="2021-05-29-campolocal_7402810b6f48472876bc851c11b76b5d9c9a58b8.png" /> planos. `T_all` tiene la interacción <img src="ltximg/2021-05-29-campolocal_d7fa01be7fa1586abf0e34d4303b78a9e3f445ee.png" alt="2021-05-29-campolocal_d7fa01be7fa1586abf0e34d4303b78a9e3f445ee.png" /> en el sitio
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
<img src="ltximg/2021-05-29-campolocal_fbc55bbd625d5e6e6a4939e86ca1dc30d736b0f2.png" alt="2021-05-29-campolocal_fbc55bbd625d5e6e6a4939e86ca1dc30d736b0f2.png" /> para <img src="ltximg/2021-05-29-campolocal_db8171ab229270b097d56ebd557b3f3faf4f2724.png" alt="2021-05-29-campolocal_db8171ab229270b097d56ebd557b3f3faf4f2724.png" /> menor a cero o <img src="ltximg/2021-05-29-campolocal_db8171ab229270b097d56ebd557b3f3faf4f2724.png" alt="2021-05-29-campolocal_db8171ab229270b097d56ebd557b3f3faf4f2724.png" /> mayor al ancho de la
película. Entonces, para los sitios <img src="ltximg/2021-05-29-campolocal_af1ba3fee9cfd7492c332193a53122760de1a917.png" alt="2021-05-29-campolocal_af1ba3fee9cfd7492c332193a53122760de1a917.png" />, <img src="ltximg/2021-05-29-campolocal_5bae3b05138450bffff94796ab739eec0a083daa.png" alt="2021-05-29-campolocal_5bae3b05138450bffff94796ab739eec0a083daa.png" /> y
para los sitios <img src="ltximg/2021-05-29-campolocal_5b90cbabc3962ac927fca2c0f57b5f7908d32e4e.png" alt="2021-05-29-campolocal_5b90cbabc3962ac927fca2c0f57b5f7908d32e4e.png" />, <img src="ltximg/2021-05-29-campolocal_11f6b7176f50ab9bf7abd45815dd63445abd8426.png" alt="2021-05-29-campolocal_11f6b7176f50ab9bf7abd45815dd63445abd8426.png" />, correspondientes a
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

Podemos correrlo como a continuación para la superficie <img src="ltximg/2021-05-29-campolocal_96de9f4a71e27ad8d36c81f68d00dc27810a57c6.png" alt="2021-05-29-campolocal_96de9f4a71e27ad8d36c81f68d00dc27810a57c6.png" /> de
una red cúbica <img src="ltximg/2021-05-29-campolocal_8157a3568d1424b8995be3036f4466bbaa77a619.png" alt="2021-05-29-campolocal_8157a3568d1424b8995be3036f4466bbaa77a619.png" /> <img src="ltximg/2021-05-29-campolocal_9a656ed868bd8e8eea38eda61367322f7fadda31.png" alt="2021-05-29-campolocal_9a656ed868bd8e8eea38eda61367322f7fadda31.png" />, <img src="ltximg/2021-05-29-campolocal_022a58ac63b5657a3715450c981dda87341b0fce.png" alt="2021-05-29-campolocal_022a58ac63b5657a3715450c981dda87341b0fce.png" />, truncando
la red recíproca en <img src="ltximg/2021-05-29-campolocal_5e1f266e0d3f4865267e4e7cbf050ed14b4c644b.png" alt="2021-05-29-campolocal_5e1f266e0d3f4865267e4e7cbf050ed14b4c644b.png" />, permitiendo interacciones con
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

Ahora repito el cálculo pero truncando la red recíproca en <img src="ltximg/2021-05-29-campolocal_d0a68357c737270eaada8645f38ac23edf20dd09.png" alt="2021-05-29-campolocal_d0a68357c737270eaada8645f38ac23edf20dd09.png" />,

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

Dado un campo externo normalizado <img src="ltximg/2021-05-29-campolocal_a6584c4d86483622c7956613a9dab3f8d679c04d.png" alt="2021-05-29-campolocal_a6584c4d86483622c7956613a9dab3f8d679c04d.png" />, podemos obtener la polarización de
bulto <img src="ltximg/2021-05-29-campolocal_77491bcf9bc2718f8ae141c192198a30362b4e58.png" alt="2021-05-29-campolocal_77491bcf9bc2718f8ae141c192198a30362b4e58.png" /> y el dipolo de bulto <img src="ltximg/2021-05-29-campolocal_ef6f095306f32e69b82432254d44392c87f2b8c6.png" alt="2021-05-29-campolocal_ef6f095306f32e69b82432254d44392c87f2b8c6.png" />.

    # name: pB
    my $PB=$dir_i==2?(1-1/$epsilon)/(4*PI):($epsilon-1)/(4*PI);
    my $pB=$PB/$density; # dipole moment

Usando Claussius Mossoti <img src="ltximg/2021-05-29-campolocal_46038841cebc16af5ee182e24bebfee43bbadb03.png" alt="2021-05-29-campolocal_46038841cebc16af5ee182e24bebfee43bbadb03.png" />
también podemos obtener la polarizabilidad <img src="ltximg/2021-05-29-campolocal_e2c293158c3637fe6f8e64df392e83613506a535.png" alt="2021-05-29-campolocal_e2c293158c3637fe6f8e64df392e83613506a535.png" />,

    # name: alpha
    my $alpha=3/(4*PI*$density)*($epsilon-1)/($epsilon+2);

La ecuación a resolver es


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_4727ef72b91361646cc0d53ad85643d535959604.png" alt="2021-05-29-campolocal_4727ef72b91361646cc0d53ad85643d535959604.png" />
</span>
<span class="equation-label">
17
</span>
</div>

La ecuación en el bulto es


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_9dcf9659a891eb480022626119a3a83acdec660b.png" alt="2021-05-29-campolocal_9dcf9659a891eb480022626119a3a83acdec660b.png" />
</span>
<span class="equation-label">
18
</span>
</div>

Restando,


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_f88d277876e7290f3b55e62428c73c377a6af055.png" alt="2021-05-29-campolocal_f88d277876e7290f3b55e62428c73c377a6af055.png" />
</span>
<span class="equation-label">
19
</span>
</div>

que reescribimos como


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_c38a533db78d4d580d6fcd7c0efda2dc4d7d84f0.png" alt="2021-05-29-campolocal_c38a533db78d4d580d6fcd7c0efda2dc4d7d84f0.png" />
</span>
<span class="equation-label">
20
</span>
</div>

donde <img src="ltximg/2021-05-29-campolocal_6ae46d6293395257e74b1c1f81c90c04e6fda2c7.png" alt="2021-05-29-campolocal_6ae46d6293395257e74b1c1f81c90c04e6fda2c7.png" /> es el tensor identidad y <img src="ltximg/2021-05-29-campolocal_8f3844e20a98c142748ae213ab4bc5a357433cd1.png" alt="2021-05-29-campolocal_8f3844e20a98c142748ae213ab4bc5a357433cd1.png" /> es la suma de las interacciones con
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
por uno de los lados, i.e. redefiniendo las <img src="ltximg/2021-05-29-campolocal_ff3d5a4e427e0c838562ac7a819d46c02b2c18ec.png" alt="2021-05-29-campolocal_ff3d5a4e427e0c838562ac7a819d46c02b2c18ec.png" />'s. Para ello,
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

Comparando con los resultados de la sección anterior vemos que <img src="ltximg/2021-05-29-campolocal_386a6ea79d8a005b03a2a3e6b7e35ee1a927d0c9.png" alt="2021-05-29-campolocal_386a6ea79d8a005b03a2a3e6b7e35ee1a927d0c9.png" /> es esencialmente idéntica al caso anterior cerca de la superficie
mientras que ahora se hace prácticamente cero en el otro extremo.


# Respuesta superficial

Ahora podemos promediar el exceso de polarización sobre la celda unitaria e
integrarla sobre la coordenada normal para obtener la corriente superficial


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_6dccbee6de6847f3e633f815b7669e056ddd42f7.png" alt="2021-05-29-campolocal_6dccbee6de6847f3e633f815b7669e056ddd42f7.png" />
</span>
<span class="equation-label">
21
</span>
</div>

De aquí podemos identificar las conductividades superficiales,


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_4ec06f4803abe8be0e4e26fd8a83a3d39a7a2b87.png" alt="2021-05-29-campolocal_4ec06f4803abe8be0e4e26fd8a83a3d39a7a2b87.png" />
</span>
<span class="equation-label">
22
</span>
</div>

donde <img src="ltximg/2021-05-29-campolocal_4ebe49d4e7859f1e4377b796dcde4769fa88b7d9.png" alt="2021-05-29-campolocal_4ebe49d4e7859f1e4377b796dcde4769fa88b7d9.png" /> es el área de la celda unitaria 2D, supusimos que <img src="ltximg/2021-05-29-campolocal_df31d015047b8f295bdd4852749fef2fa6e6b463.png" alt="2021-05-29-campolocal_df31d015047b8f295bdd4852749fef2fa6e6b463.png" />, <img src="ltximg/2021-05-29-campolocal_407c076cb2de6eb8dc1357b587952b56238f7c50.png" alt="2021-05-29-campolocal_407c076cb2de6eb8dc1357b587952b56238f7c50.png" />,
y <img src="ltximg/2021-05-29-campolocal_3612876dfbe476ef94d2b3f426edd001d067800b.png" alt="2021-05-29-campolocal_3612876dfbe476ef94d2b3f426edd001d067800b.png" /> son direcciones principales y que
usamos campos normalizados <img src="ltximg/2021-05-29-campolocal_fea927cb84acbfa17e7185427e85c2dcdc5ac1d4.png" alt="2021-05-29-campolocal_fea927cb84acbfa17e7185427e85c2dcdc5ac1d4.png" /> al calcular <img src="ltximg/2021-05-29-campolocal_f4a6244f44969535cb91145b97dc163489085f97.png" alt="2021-05-29-campolocal_f4a6244f44969535cb91145b97dc163489085f97.png" />, <img src="ltximg/2021-05-29-campolocal_d0b15f4dff5bb9664b81be6bb16a99140ecf35b5.png" alt="2021-05-29-campolocal_d0b15f4dff5bb9664b81be6bb16a99140ecf35b5.png" /> y <img src="ltximg/2021-05-29-campolocal_e953f7d8bdb16ab9a11936a4d6ae075ec8861098.png" alt="2021-05-29-campolocal_e953f7d8bdb16ab9a11936a4d6ae075ec8861098.png" /> al
calcular <img src="ltximg/2021-05-29-campolocal_e58c4156ea30dd82328bf8bbe6c21d621474cfb0.png" alt="2021-05-29-campolocal_e58c4156ea30dd82328bf8bbe6c21d621474cfb0.png" />.

Con estas funciones respuesta puedo calcular la impedancia superficial


<div class="equation-container">
<span class="equation">
<img src="ltximg/2021-05-29-campolocal_da03853f9fa53bed9d43e450749cd3c64accd86e.png" alt="2021-05-29-campolocal_da03853f9fa53bed9d43e450749cd3c64accd86e.png" />
</span>
<span class="equation-label">
23
</span>
</div>

donde elegimos las componentes apropiadas de acuerdo a la polarización
y a la orientación del plano de incidencia.

Por motivos prácticos tenemos que enfrentar ahora el problema de las
unidades. En general, <img src="ltximg/2021-05-29-campolocal_1b10df782ac24208c789209d1629618b22e522f6.png" alt="2021-05-29-campolocal_1b10df782ac24208c789209d1629618b22e522f6.png" />, <img src="ltximg/2021-05-29-campolocal_8d27279e6f8b4f92eb4d6cdc270d1c2cc05e3d39.png" alt="2021-05-29-campolocal_8d27279e6f8b4f92eb4d6cdc270d1c2cc05e3d39.png" />, por
lo que <img src="ltximg/2021-05-29-campolocal_73c6e94d8ad74c122b83f58a152721b4eb27e86a.png" alt="2021-05-29-campolocal_73c6e94d8ad74c122b83f58a152721b4eb27e86a.png" /> y los cocientes <img src="ltximg/2021-05-29-campolocal_a9b1f538ff4929aea0153e0d5fb48cbab36124ab.png" alt="2021-05-29-campolocal_a9b1f538ff4929aea0153e0d5fb48cbab36124ab.png" /> y <img src="ltximg/2021-05-29-campolocal_8b3f6d3174e8fc7eef94ec34692bb0c9bd761da0.png" alt="2021-05-29-campolocal_8b3f6d3174e8fc7eef94ec34692bb0c9bd761da0.png" /> son adimensionales. Al normalizar los campos a 1 y desproveerlos de unidades,
los dipolos calculados arriba tendrían unidades de volumen en lugar de
carga por distancia, puesto que la polarizabilidad tiene unidades de
volumen. Al dividirlos entre <img src="ltximg/2021-05-29-campolocal_4ebe49d4e7859f1e4377b796dcde4769fa88b7d9.png" alt="2021-05-29-campolocal_4ebe49d4e7859f1e4377b796dcde4769fa88b7d9.png" /> adquirirían unidades de distancia y
al multiplicarlos por <img src="ltximg/2021-05-29-campolocal_817023e3b92e52d3364235a645ce224e05214ded.png" alt="2021-05-29-campolocal_817023e3b92e52d3364235a645ce224e05214ded.png" /> llegaríamos a las esperadas unidades de
velocidad. Es común expresar la frecuencia en términos de la energía
<img src="ltximg/2021-05-29-campolocal_b19d3e7bf1c3d143745a472e7278d5035cba94b3.png" alt="2021-05-29-campolocal_b19d3e7bf1c3d143745a472e7278d5035cba94b3.png" /> en unidades de <img src="ltximg/2021-05-29-campolocal_15d4b0315859ebdb77229febe9a9617e1fb04b3b.png" alt="2021-05-29-campolocal_15d4b0315859ebdb77229febe9a9617e1fb04b3b.png" />. Por otro lado, es cómodo expresar
los vectores de la base cristalina <img src="ltximg/2021-05-29-campolocal_45bbfb41e2582051ce882eb9054c5cbd3782465c.png" alt="2021-05-29-campolocal_45bbfb41e2582051ce882eb9054c5cbd3782465c.png" />, <img src="ltximg/2021-05-29-campolocal_d16babec75d9952675f9a08a292932936e899c02.png" alt="2021-05-29-campolocal_d16babec75d9952675f9a08a292932936e899c02.png" /> y <img src="ltximg/2021-05-29-campolocal_f719d5849b622408ce423485031ff0992b2e9dd4.png" alt="2021-05-29-campolocal_f719d5849b622408ce423485031ff0992b2e9dd4.png" /> en
unidades del parámetro de red del sistema. Entonces, la velocidad de la luz arriba
<img src="ltximg/2021-05-29-campolocal_5ab8203e7ca7262a895a80fd6729292ac053c39e.png" alt="2021-05-29-campolocal_5ab8203e7ca7262a895a80fd6729292ac053c39e.png" /> deberíamos expresarla en unidades consistentes, por ejemplo,
eV <img src="ltximg/2021-05-29-campolocal_34904c46a49935dc0a4d8ad5c652f831708e37e4.png" alt="2021-05-29-campolocal_34904c46a49935dc0a4d8ad5c652f831708e37e4.png" /> parámetro de red. Para ello usamos el factor de conversión
<img src="ltximg/2021-05-29-campolocal_d9ac405ecf8bdb82745f6f9d3e33a112ece143e7.png" alt="2021-05-29-campolocal_d9ac405ecf8bdb82745f6f9d3e33a112ece143e7.png" /> e leemos el parámetro de red en
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
<img src="ltximg/2021-05-29-campolocal_f796ac16360cd5bf4d5dd9df17384cb600e96963.png" alt="2021-05-29-campolocal_f796ac16360cd5bf4d5dd9df17384cb600e96963.png" /> desde la línea de comandos, leeremos el nombre de un
archivo con una tabla de valores de frecuencia, <img src="ltximg/2021-05-29-campolocal_4938810586faf94d0f90fc198d4e7f24690b7767.png" alt="2021-05-29-campolocal_4938810586faf94d0f90fc198d4e7f24690b7767.png" /> y
<img src="ltximg/2021-05-29-campolocal_b1aad222f82d66ddc7bc8cfc7212b03a4ed766e3.png" alt="2021-05-29-campolocal_b1aad222f82d66ddc7bc8cfc7212b03a4ed766e3.png" /> para, y para cada valor obtendremos la impedancia
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

Lo volvemos a correr pero ahora a un ángulo de incidencia <img src="ltximg/2021-05-29-campolocal_bc779de61617c0c73175c0356a0bf814f08c227a.png" alt="2021-05-29-campolocal_bc779de61617c0c73175c0356a0bf814f08c227a.png" />.

    ./DeltaR.pl -a .7071,0 -b 0,1 -c .3536,.5,.3536 \
         -pqmax 3 -dmax 5 -N 5 -lattice .54 -angle 45 \
         -ifilename epsSiAsp.dat -ofilename si110-45.png \
         -title 'Anisotropía (R_y-R_x)/R para Si (110) {/Symbol Q}_i=45'

![img](../../../../assets/image/20210529si110-45.png)

Curiosamente, aunque la respuesta normal es la misma para ambas
polarizaciones, como <img src="ltximg/2021-05-29-campolocal_b49594828da043411bf085b5fb425f746e90b512.png" alt="2021-05-29-campolocal_b49594828da043411bf085b5fb425f746e90b512.png" /> es menor, la anisotropía relativa es
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
