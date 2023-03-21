---
layout: post
title: Complex Analysis
author: Saurish Chakrabarty
categories: journal
tags: [documentation,sample]
---
## Syllabus
- About complex numbers
  - Euler's formula
  - de Moivre's theorem
  - Roots of complex numbers
  - Triangle inequality
  - Schwarz inequality
- Functions of complex variables
  - Limits and continuity
  - Analyticity and Cauchy-Riemann conditions
  - Harmonic function
  - Examples of analytic functions
  - Singular functions
    - Poles
    - Branch points
    - Order of singularity
    - Branch cut
- Integration of a function of a complex variable
  - Cauchy's inequality
  - Cauchy's integral formula
  - Residues and residue theorem
  - Application in solving definite integrals
- Simply and multiply connected regions
- Laurent and Taylor series expansions

A complex number $z$ is an ordered pair of real numbers $(x,y)$ with
addition and multiplication defined as follows. For two complex
numbers $z_1=(x_1,y_1)$ and $z_2=(x_2,y_2)$,
$z_1+z_2\equiv(x_1+x_2,y_1+y_2)$
$z_1z_2\equiv(x_1x_2-y_1y_2,x_1y_2+y_1x_2)$. Real and imaginary
numbers correspond to numbers of the form $(x,0)$ and $(0,y)$
respectively. The complex number $(0,1)$ is denoted by $i$. Thus,
```math
\begin{matrix}i^2&=&(-1,0)&\equiv&-1\\z&=&(x,0)+i(y,0)&\equiv&x+iy\end{matrix}
```
The real and imaginary parts of a complex number are denoted as follows.
$$
  \mbox{Re }z=x,
  \mbox{ and Im }z=y
$$
$$`
  \mbox{Re }z=x,
  \mbox{ and Im }z=y
`$$
The set of all complex numbers is denoted by the symbol $\mathbb C$.
### Aside: Field of complex numbers
The set $\mathbb C$ forms field under addition and
multiplication. This has the following requirements.
- Ring under addition and multiplication.
  - Abelian group under addition.
    - Closure: $z_1+z_2\in\mathbb C$.
    - Associativity: $z_1+(z_2+z_3)=(z_1+z_2)+z_3$.
    - Existence of identity: $\exists0\in\mathbb C$, such that
      $z+0=0+z=z$. 
    - Existence of inverses: For each $z$, $\exists-z\in\mathbb C$, such that
      $z+(-z)=-z+z=0$. 
    - Commutativity: $z_1+z_2=z_2+z_1$.
  - Commutative semigroup under multiplication.
    - Closure: $z_1z_2\in\mathbb C$.
    - Associativity: $z_1(z_2z_3)=(z_1z_2)z_3$.
    - Commutativity: $z_1z_2=z_2z_1$.
- Existence of a multiplicative identity (1):
  $z\times1=1\times z=z$.
- Existence of multiplicative inverses for all elements other than
  the additive identity (0):
  For $z\neq0$, $zz^{-1}=z^{-1}z=1$.
