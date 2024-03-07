---
layout: post
title: Presentations in Org
comments: true
excerpt: Epresent allows trivial presentations of org mode files.
tags:
       - perl

---


# Epresent

I can use epresent to make simple presentations out of org mode files.

[User's guide](https://github.com/eschulte/epresent/blob/master/README.org). As it is only a few lines long, I reproduce it here.


## Install

Just install epresent from melpa repository.


## Usage

1.  Call epresent-run on an org-buffer.
2.  press t / 1 to view the top level of the presentation navigate the
    presentation with n/f, p/b
3.  scroll with k and l
4.  use c and C to navigate between code blocks, e to edit them, x to
    make it run, and s / S to toggle their visibility quit with q
    1.  It is necessary to set `org-confirm-babel-evaluate~` to nil, maybe
        as a file local variable, so that `x` evaluates the code without
        asking.


## Hints

1.  It may be useful to set the local variable
    `org-confirm-babel-evaluate` in order to evaluate code
    interactively without having to confirm in another window, which
    may be confusing. Use code as:
    
        # Local Variables:
        # org-confirm-babel-evaluate: nil
        # End:
    
    at the end of the file.
2.  However, you might have to confirm in another window the use of
    local variables when starting and finishing the presentation.
3.  Images may be included.

