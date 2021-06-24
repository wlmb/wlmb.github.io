---
layout: post
title: Nonlocal multicomponent metamaterials
comments: true
excerpt: Slides of the talk given at the MexSIAM Annual Meeting 2021, June 23, 2021
tags:
   - homogenization
   - metamaterials
   - physics
   - talks
---

The slides of the talk *Nonlocal multicomponent metamaterials* I gave
at the MexSIAM Annual Meeting 2021 on June 23, 2021 can be found
[here](/assets/pdf/20210624talk.pdf). Using a spinor-like
representation, I can extend the calculation of the macroscopic
response of a metamaterial to multicomponent systems with and without
retardation. The trick is to use an *Euclidean* instead of a
*Hermitian* inner product to define matrix elements, and to use a
spinor like representation of the fields, with two *components* `+k`
and `-k`, corresponding to Bloch waves moving in opposite
directions. This way, all relevant operators become symmetric, even
when there is dissipation, and I can use some of the usual *linear
algebra* theorems about orthogonality to build a Haydock
representation that allows an efficient calculation of the macroscopic
response and the microscopic fields. Some tests are shown to verify
that the formalism works. The ideas were published [here](https://doi.org/10.1002/pssb.201900560). They have
been implemented in the `Photonic` package ([link1](https://github.com/wlmb/Photonic) and [link2](https://metacpan.org/pod/Photonic)).
