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

    import three;
    currentprojection=orthographic(5,4,2,center=true);
    currentlight=(0,10,20);
    size(30cm);
    //size3(6cm,5cm,8cm);
    pen c[] ={black, red, green, pink, yellow, lightblue, purple, white, brown, mediumblue, orange};
    int N=10;
    real f=1/N;
    for(int i=N; i>0; --i){
      for(int j=0;j<i;++j){
        draw(scale3(f)*shift(j,i-1,N-i)*unitcube, c[i]+opacity(0.9));
        draw(scale3(f)*shift(i-1,j,N-i)*unitcube, c[i]+opacity(0.9));
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
    	 *path3(texpath("$"+(string)(i*(j+1))+"$"), XYplane),
          white+linewidth(4));
        draw(scale3(f)*shift(.5,.5,1.05)*shift(j,i-1,N-i)
    	 *scale3(.05)*rotate(90,Z)
    	 *path3(texpath("$"+(string)(i*(j+1))+"$"), XYplane),
    	 white+linewidth(4));
        draw(scale3(f)*shift(1.05,.5,0.5)*shift(i-1,j,N-i)
    	 *scale3(.05)*rotate(90,Y)*rotate(90,Z)
    	 *path3(texpath("$"+(string)(i*(j+1))+"$"), XYplane),
    	 white+linewidth(4));
        draw(scale3(f)*shift(.5,1.05,0.5)*shift(j,i-1,N-i)
    	 *scale3(.05)*rotate(90,Z)*rotate(90,Y)*rotate(90,3Z)
    	 *(path3(texpath("$"+(string)(i*(j+1))+"$"), XYplane)),white+linewidth(4));
      }
    }

![img](../../../../assets/image/multiplication.png)

I had some difficulty with the numbers. I could convert numbers to
paths, to 3D paths and then to surfaces, but when I drew them
asymptote filled the holes. Thus, I traced the outlines with a thick
pen. There must be a better way though.
