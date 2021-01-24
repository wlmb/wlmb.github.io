---
layout: post
title: Fun with asymptote
comments: true
excerpt: Virtual material for a Montessori school in Asymptote
tags:
   - asymptote
---


# Multiplication table

Discussing about a possible virtual material for a Montessori school,
I got the idea that I could use it to learn some `Asymptote`. Thus, I
present below an asymptote code that produces a partial multiplication
table, step by step, forming a nice pyramid, using the Montessori
color scheme for the floors.

    //texpreamble("\usepackage{mathptmx}");
    //texpreamble("\usepackage{helvet}");
    //texpreamble("\usepackage{avant}");
    import three;
    currentprojection=orthographic(5,4,3,center=true);
    currentlight=light(background=white,specularfactor=0,specular=white,(0,10,20));
    size(30cm);
    defaultpen(AvantGarde());
    //size3(6cm,5cm,8cm);
    pen c[] ={black, red, green, pink, yellow, lightblue, purple, white, brown, mediumblue, orange};
    defaultpen(AvantGarde());
    int N=10;
    real f=1/N;
    for(int i=N; i>0; --i){
      for(int j=0;j<i;++j){
        draw(scale3(f)*shift(j,i-1,N-i)*unitcube, c[i]);
        draw(scale3(f)*shift(i-1,j,N-i)*unitcube, c[i]);
      }
    }
    for(int i=N; i>0; --i){
      for(int j=0;j<i;++j){
        draw(scale3(f)*shift(i-1,j,N-i)*unitbox, white+linewidth(2));
        draw(scale3(f)*shift(j,i-1,N-i)*unitbox, white+linewidth(2));
      }
    }
    for(int i=N; i>0; --i){
      for(int j=0;j<i;++j){
        draw(scale3(f)*shift(.5,.5,1.05)*shift(i-1,j,N-i)
    	 *scale3(.05)*rotate(90,Z)
    	 *surface(texpath((string)(i*(j+1)))),
    	 white, nolight);
        draw(scale3(f)*shift(.5,.5,1.05)*shift(j,i-1,N-i)
    	 *scale3(.05)*rotate(90,Z)
    	 *surface(texpath((string)(i*(j+1)))),
    	 white, nolight);
        draw(scale3(f)*shift(1.05,.5,0.5)*shift(i-1,j,N-i)
    	 *scale3(.05)*rotate(90,Y)*rotate(90,Z)
    	 *surface(texpath((string)(i*(j+1)))),
    	 white, nolight);
        draw(scale3(f)*shift(.5,1.05,0.5)*shift(j,i-1,N-i)
    	 *scale3(.05)*rotate(90,Z)*rotate(90,Y)*rotate(90,3Z)
    	 *surface(texpath((string)(i*(j+1)))),
    	 white,nolight);
      }
    }

![img](../../../../assets/image/multiplication.png)

The following code separates vertically the planes so you can peek
beneath them. The problem is that drawing so many cubes
(10\*11\*21/6=385) is too much work for Asymptote (the heap is depleted). I could have drawn
each plane as a square prism, but I just added a second row to each plane.

    //texpreamble("\usepackage{mathptmx}");
    //texpreamble("\usepackage{helvet}");
    //texpreamble("\usepackage{avant}");
    import three;
    currentprojection=orthographic(5,4,3,center=true);
    currentlight=light(background=white,specularfactor=0,specular=white,(0,10,20));
    size(30cm);
    defaultpen(AvantGarde());
    //size3(6cm,5cm,8cm);
    pen c[] ={black, red, green, pink, yellow, lightblue, purple, white, brown, mediumblue, orange};
    defaultpen(AvantGarde());
    int N=10;
    real f=1/N;
    for(int i=N; i>0; --i){
      for(int j=0;j<i;++j){
        draw(scale3(f)*shift(j,i-1,(N-i)*1.45)*unitcube, c[i]);
        draw(scale3(f)*shift(i-1,j,(N-i)*1.45)*unitcube, c[i]);
        if(i>1){
          draw(scale3(f)*shift(j,i-2,(N-i)*1.45)*unitcube, c[i]);
          draw(scale3(f)*shift(i-2,j,(N-i)*1.45)*unitcube, c[i]);
        }
      }
    }
    for(int i=N; i>0; --i){
      for(int j=0;j<i;++j){
        draw(scale3(f)*shift(i-1,j,(N-i)*1.45)*unitbox, white+linewidth(2));
        draw(scale3(f)*shift(j,i-1,(N-i)*1.45)*unitbox, white+linewidth(2));
        if(i>1){
          draw(scale3(f)*shift(i-2,j,(N-i)*1.45)*unitbox, white+linewidth(2));
          draw(scale3(f)*shift(j,i-2,(N-i)*1.45)*unitbox, white+linewidth(2));
        }
      }
    }
    for(int i=N; i>0; --i){
      for(int j=0;j<i;++j){
        draw(scale3(f)*shift(.5,.5,1.05)*shift(i-1,j,(N-i)*1.45)
    	 *scale3(.05)*rotate(90,Z)
    	 *surface(texpath((string)(i*(j+1)))),
    	 white, nolight);
        draw(scale3(f)*shift(.5,.5,1.05)*shift(j,i-1,(N-i)*1.45)
    	 *scale3(.05)*rotate(90,Z)
    	 *surface(texpath((string)(i*(j+1)))),
    	 white, nolight);
        draw(scale3(f)*shift(1.05,.5,0.5)*shift(i-1,j,(N-i)*1.45)
    	 *scale3(.05)*rotate(90,Y)*rotate(90,Z)
    	 *surface(texpath((string)(i*(j+1)))),
    	 white, nolight);
        draw(scale3(f)*shift(.5,1.05,0.5)*shift(j,i-1,(N-i)*1.45)
    	 *scale3(.05)*rotate(90,Z)*rotate(90,Y)*rotate(90,3Z)
    	 *surface(texpath((string)(i*(j+1)))),
    	 white,nolight);
        if(i>1){
          draw(scale3(f)*shift(.5,.5,1.05)*shift(i-2,j,(N-i)*1.45)
    	   *scale3(.05)*rotate(90,Z)
    	   *surface(texpath((string)((i-1)*(j+1)))),
    	   white, nolight);
          draw(scale3(f)*shift(.5,.5,1.05)*shift(j,i-2,(N-i)*1.45)
    	   *scale3(.05)*rotate(90,Z)
    	   *surface(texpath((string)((i-1)*(j+1)))),
    	   white, nolight);
        }
      }
    }

![img](../../../../assets/image/multiplicationSeparated.png)
