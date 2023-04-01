---
layout: post
title: "About Complex Numbers"
author: "Saurish Chakrabarty"
categories: journal
tags: [documentation,sample]
---
A complex number $z$ is an ordered pair of real numbers $(x,y)$ with
addition and multiplication defined as follows. For two complex
numbers $z_1=(x_1,y_1)$ and $z_2=(x_2,y_2)$,
$z_1+z_2\equiv(x_1+x_2,y_1+y_2)$
$z_1z_2\equiv(x_1x_2-y_1y_2,x_1y_2+y_1x_2)$. Real and imaginary
numbers correspond to numbers of the form $(x,0)$ and $(0,y)$
respectively. The complex number $(0,1)$ is denoted by $i$. Thus,
<p style="text-align: center;">$i^2=(-1,0)\equiv-1$ and $z=(x,0)+i(y,0)\equiv x+iy$.</p>
The real and imaginary parts of a complex number are denoted as follows.
<p style="text-align: center;">Re $z$ = $x$ and Im $z$ = $y$.</p>
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

Exercise: For a complex number, $z=x+iy$, obtain the real and imaginary parts of $1/z$.

### Geometric Interpretation of complex numbers
A complex number $z=x+iy$, can be viewed as a point $(x,y)$ in the $xy$-plane. The $xy$-plane is then also known as the $z$-plane or the complex plane. The distance of the point $(x,y)$ from the origin of the complex plane is known as the _modulus_ of the complex number $z$ and is denoted by $|z|$. It is easy to check that $|z_1-z_2|$ is the distance between the points $z_1$ and $z_2$. This, in turn, implies that $|z-z_0|=R$ is the equation of a circle of radius $R$ whose centre is at $z_0$.

### Complex Conjugate
The complex conjugate $\bar{Z}$, of a complex number $z=x+iy$ is the complex number $x-iy$. It is easy to check the following identities.

$$
|z|=|\bar{z}|\\
z\bar{z}=|z|^2=|\bar{z}|^2\\
z+\bar{z}=2\ \text{Re }z\\
z-\bar{z}=2i\ \text{Im }z\\
|z_1z_2|=|z_1||z_2|
$$

Let us discuss some inequalities involving moduli of complex numbers. 

#### Triangle Inequality
Since $\lvert z\rvert^2=(\text{Re }z)^2+(\text{Im }z)^2$, it follows that $\lvert z\rvert\ge\lvert\text{Re }z\rvert\ge\text{Re }z$ and $\lvert z\rvert\ge\lvert\text{Im }z\rvert\ge\text{Im }z$. This can be used to establish the _triangle inequality_.

$$
|z_1+z_2|\le|z_1|+|z_2|
$$

The proof of this is as follows.

$$
\left|z_1+z_2\right|^2=\left(z_1+z_2\right)\left(\overline{z_1+z_2}\right)\\
=\left|z_1\right|^2+\left|z_2\right|^2+z_1\overline{z_2}+z_2\overline{z_1}\\
=\left|z_1\right|^2+\left|z_2\right|^2+2\text{Re }z_1\overline{z_2}\\
\le\left|z_1\right|^2+\left|z_2\right|^2+2\left|z_1\right|\left|z_2\right|\\
\Rightarrow\left|z_1+z_2\right|^2\le\left(\left|z_1\right|+\left|z_2\right|\right)^2\\
\Rightarrow\left|z_1+z_2\right|\le\left|z_1\right|+\left|z_2\right|
$$

In arriving at the final inequality from the one in the second last line, 
we use the fact that the quantities that are being squared on both sides of the 
second last line are positive.

### Polar Representation
Using the polar coordinates for the two dimensional complex plane results in the 
polar representation of a complex number. The radial coordinate is the _modulus_ of 
the complex number and the polar angle is known as its _argument_. Thus, for a complex
number $z=x+iy$,

$$
\text{mod }z=|z|=\sqrt{x^2+y^2}\\
\text{arg }z=\tan^{-1}\frac{y}{x}
$$

The principal value of the argument of a complex number is represented by Arg $z$ and is chosen to
take values in the range $[-\pi,\pi]$.

> __Tip:__ In python, you can use the `arctan2` function to get the polar angle directly in the correct quadrant. Functions with similar names are also available in other programming languages.

It is easy to check that the argument of the product of two complex numbers is the sum of their arguments.

### Exponential Form / Euler's formula

$$
e^{i\theta}=\cos\theta+i\sin\theta\equiv\text{cis }\theta
$$

To see where this comes from, expand the left hand side and use the fact that $i^2=-1$.

Thus, using the above polar representation, any complex number $z$ can be written as $re^{i\theta}$, where $r=\lvert z\rvert$ and $\theta=\text{arg }z$.


[Back to syllabus](https://saurishc.github.io/complex)
