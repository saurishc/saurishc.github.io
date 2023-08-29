---
layout: post
title: "Basic Physics of Fluids"
author: "Saurish Chakrabarty"
categories: journal
tags: [documentation,sample]
---

## Distinction between Solids and Fluids
When we interact with a solid (apply a force on it), it bends (deforms/changes shape) -- the amount of deformation depends on the force. When we apply a force on a liquid, it flows -- its deformation increases with time. Many materials exhibit both solid-like and fluid-like characters (viscoelastic materials). In this course, we will discuss only simple fluids in which arbitrarily small forces result in macroscopic deformations (change in relative positions of its elements).

## The Continuum Hypothesis

In the study of fluids, we are interested in macroscopic phenomena. The fluid is treated as a continuous medium. An arbitrarily small element of the fluid contains a large number of molecules. An arbitrarily small element is small compared to the size of the system being studied but is large compared to intermolecular separations. In this picture, phrases such as molecular positions and molecular speeds are ill-defined. A _fluid particle_ should be thought of as a volume element in the fluid containing a large number of molecules.

A fluid is described by the distribution of velocities of the fluid particles in space and time and the distribution of any two thermodynamic quantities, such as the density and the pressure -- $\vec{v}(\vec{r},t)$, $p(\vec{r},t)$ and $\rho(\vec{r},t)$. Thus, five fields (functions of space and time) describe the state of a fluid.

### Typical Numbers justifying Continuum Hypothesis

Linear dimension of system: $1 cm$ \
Linear dimension of volume element: $0.001 cm$ \
Number of molecules in volume element: $2.5\times10^{10}$ \
(assuming the system to be air, $\rho=2.5\times10^{19} cm^{-3}$)

## Equation of Continuity

Let us consider an arbitrary volume, $V_0$, in a fluid. The mass of the fluid contained in this volume is given by $\int\rho\ dV$. The amount of fluid which flows out of $V_0$ per unit time is given by,

$$
\oint \rho\vec{v}.\overrightarrow{dS},
$$

where the integral is over the closed surface surrounding $V_0$. Using Gauss's divergence theorem, this can also be written as,

$$
\oint \vec{\nabla}\cdot\left(\rho\vec{v}\right)dV
$$

The decrease in mass of the liquid in $V_0$ per unit time can be written as,

$$
\frac{d}{dt}\int\rho dV=\int\frac{\partial\rho}{\partial t}dV
$$

This decrease can only be because of fluid particles moving out of $V_0$. Thus,

$$
\int\left(\frac{\partial\rho}{\partial t}+\vec{\nabla}\cdot\left(\rho\vec{v}\right)\right)dV=0
$$

Since this must be true for any volume, the integrand itself must be zero at any point in the fluid, _i.e._,

$$
\frac{\partial\rho}{\partial t}+\vec{\nabla}\cdot\left(\rho\vec{v}\right)=0
$$

This is known as the _equation of continuity_. Here, $\rho\vec{v}$ represents the _mass flux density_, $\vec{j}$.

## Euler's Equation

The total force acting on an arbitrary volume $V_0$ in a fluid is the sum of the forces on the elements of the surrounding surface. Thus,

$$
-\oint p\ \overrightarrow{dS}=-\int\vec{\nabla}p\ dV
$$

---

The above step uses the following theorem which can be derived from Gauss's theorem. For any scalar field, $\phi$,

$$
\oint \phi\ \overrightarrow{dS}=\int\vec{\nabla}\phi\ dV
$$

Proof:

$$
\int \vec{\nabla}\phi\ dV
=\int \left(\hat{i}\frac{\partial\phi}{\partial x}+\hat{j}\frac{\partial\phi}{\partial y}+\hat{k}\frac{\partial\phi}{\partial z}\right)dV
=\hat{i}\int\vec{\nabla}\cdot\left(\hat{i}\phi\right)dV+\hat{j}\int\vec{\nabla}\cdot\left(\hat{j}\phi\right)dV+\hat{k}\int\vec{\nabla}\cdot\left(\hat{k}\phi\right)dV
$$

$$
\Rightarrow
\int \vec{\nabla}\phi\ dV
=\hat{i}\int\left(\hat{i}\phi\right)\cdot\overrightarrow{dS}+\hat{j}\int\left(\hat{j}\phi\right)\cdot\overrightarrow{dS}+\hat{k}\int\left(\hat{k}\phi\right)\cdot\overrightarrow{dS}=\int \phi\left(\hat{i}dS_x+\hat{j}dS_y+\hat{k}dS_z\right)=\int\phi\ \overrightarrow{dS}
$$

---

Thus, the force on a fluid element of volume $dV$ is just $-\vec{\nabla}p\ dV$. We can therefore write down Newton's second law for this volume element.

$$
(\rho dV)\frac{d\vec{v}}{dt}=-\vec{\nabla}p\ dV\  \Rightarrow\ \rho\frac{d\vec{v}}{dt}=-\vec{\nabla}p
$$

### The meaning of $\frac{d\vec{v}}{dt}$
In the above expression, $\frac{d\vec{v}}{dt}$ represents the rate of change of the velocity of a fluid element as it moves. It is _not_ the rate of change of the fluid velocity at some point in space.
