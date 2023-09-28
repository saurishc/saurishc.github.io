---
layout: post
title: "Digital Circuits"
author: "Saurish Chakrabarty"
categories: journal
tags: [documentation,sample]
---

## Digital versus Analog
In analog circuits, the inputs and outputs can take a continuous range of values. In digital circuits, the inputs and outputs can be in two possible states, interpreted as {0, 1}
or {on, off} or {true, false}.

_Note_: In general, if a variable, $x$, can take one of two different values, say, $a$ and $b$, then, it can be linearly mapped to another variable $y$ which can be 
either zero or one. The transformation that does this is $y=\frac{x-a}{b-a}$.

## Boolean Algebra
This is the algebra of binary variables (those that can take two different values). It was introduced by George Boole in 1847.

Let $X,Y\in{0,1}$ (Boolean variable). The following are basic operations.
- **NOT**: $\overline{X}=0$ if $X=1$ and 1 if $X=0$.
- **OR(+)**: $X+Y$=0$ if both $X$ and $Y$ are 0, and 1 otherwise.
- **AND($\cdot$)**: $X\cdot Y$=1$ if both $X$ and $Y$ are 1, and 0 otherwise.

All these operations satisfy the closure property, _i.e._, the result is also a Boolean variable. This means that the output can be used as an input for another operation.

**Operator precedence**: Like in usual algebra, where we have the BODMAS rule, here too expressions inside brackets are simplified first, followed by AND operations and finally OR.
