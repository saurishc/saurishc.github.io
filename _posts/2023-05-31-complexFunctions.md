---
layout: post
title: "Functions of Complex Variables"
author: "Saurish Chakrabarty"
categories: journal
tags: [documentation,sample]
---
A function of a complex variable $f(z)$ is an ordered pair of two real functions, $u(x,y)$ and $v(x,y)$, each of two real variables,
$x=$Re $z$ and $y=$Im $z$. Thus,

$$
f(z)=u(x,y)+iv(x,y)
$$

## Graphical Representation
There are two alternative representations for a function of a complex variable.

First, we can plot the surfaces $u(x,y)$ and $v(x,y)$ on a three dimensional plot. Second, we can use another complex plane -- the $w$-plane -- to plot $w=u+iv$ corresponding to each point on the $z$-plane.

An example of a complex function is $f(z)=z^2$, for which it is easy to check that $u(x,y)=x^2-y^2$ and $v(x,y)=2xy$.

## Limits
If $f(z)$ goes arbitrarily close to $w_0$ whenever $z$ goes arbitrarily close to $z_0$, then we say that,

$$
\lim_{z\to z_0} f(z)=w_0.
$$

#### $\epsilon-\delta$ definition
The above limit is true if for any $\epsilon$ greater than zero, we can find $\delta(\epsilon)$ which is also greater than zero, such that whenever $|z-z_0|<\delta$, $|f(z)-w_0|<\epsilon$.
