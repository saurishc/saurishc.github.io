---
layout: post
title: "Basic Physics of Fluids"
author: "Saurish Chakrabarty"
categories: journal
tags: [documentation,sample]
---

## Distinction between Solids and Fluids
When we interact with a solid (apply a force on it), it bends (deforms/changes shape) -- the amount of deformation depends on the force. When we apply a force on a fluid, it flows -- its deformation increases with time.

#### Definition
_A fluid is a material in which small (suitably chosen) forces can change the relative positions of its elements by a significant (not small) amount. A fluid deforms continuously under the application of a shear stress, however small._

Many materials exhibit both solid-like and fluid-like characters (viscoelastic materials). In this course, we will discuss only simple fluids in which arbitrarily small forces result in macroscopic deformations (change in relative positions of its elements).

## The Continuum Hypothesis

In the study of fluids, we are interested in macroscopic phenomena. The fluid is treated as a continuous medium. An arbitrarily small element of the fluid contains a large number of molecules. This fluid element is small compared to the size of the system being studied but is large compared to intermolecular separations. In this picture, phrases such as molecular positions and molecular speeds are ill-defined. A _fluid particle_ should be thought of as an infinitesimal volume element in the fluid, but containing a large number of molecules.

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

The increase in mass of the liquid in $V_0$ per unit time can be written as,

$$
\frac{d}{dt}\int\rho dV=\int\frac{\partial\rho}{\partial t}dV
$$

A negative value for this implies a decrease in mass, i.e., the negative of the above quantity is the decrease in the mass of the system per unit time. This decrease can only be because of fluid particles moving out of $V_0$. Thus, equating the two expressions for the decrease in mass per unit time and rearranging, we get,

$$
\int\left(\frac{\partial\rho}{\partial t}\vec{\nabla}\cdot\left(\rho\vec{v}\right)\right)dV=0.
$$

Since this must be true for any volume, the integrand itself must be zero at any point in the fluid, _i.e._,

$$
\frac{\partial\rho}{\partial t}+\vec{\nabla}\cdot\left(\rho\vec{v}\right)=0
$$

This is known as the _equation of continuity_. Here, $\rho\vec{v}$ represents the _mass flux density_, $\vec{j}$.

## Euler's Equation

The total force acting on an arbitrary volume $V_0$ in a fluid is the sum of the forces on the elements of the surrounding surface. This force is therefore given by,

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
$$

$$
\Rightarrow
\int \vec{\nabla}\phi\ dV
=\hat{i}\int\vec{\nabla}\cdot\left(\hat{i}\phi\right)dV+\hat{j}\int\vec{\nabla}\cdot\left(\hat{j}\phi\right)dV+\hat{k}\int\vec{\nabla}\cdot\left(\hat{k}\phi\right)dV
$$

$$
\Rightarrow
\int \vec{\nabla}\phi\ dV
=\hat{i}\int\left(\hat{i}\phi\right)\cdot\overrightarrow{dS}+\hat{j}\int\left(\hat{j}\phi\right)\cdot\overrightarrow{dS}+\hat{k}\int\left(\hat{k}\phi\right)\cdot\overrightarrow{dS}
$$

$$
\Rightarrow
\int \vec{\nabla}\phi\ dV
=\int \phi\left(\hat{i}dS_x+\hat{j}dS_y+\hat{k}dS_z\right)=\int\phi\ \overrightarrow{dS}
$$

---

Thus, the force on a fluid element of volume $dV$ is just $-\vec{\nabla}p\ dV$. We can therefore write down Newton's second law for this volume element.

$$
(\rho dV)\frac{d\vec{v}}{dt}=-\vec{\nabla}p\ dV\  \Rightarrow\ \rho\frac{d\vec{v}}{dt}=-\vec{\nabla}p
$$

### The meaning of $\frac{d\vec{v}}{dt}$
In the above expression, $\frac{d\vec{v}}{dt}$ represents the rate of change of the velocity of a fluid element as it moves. It is _not_ the rate of change of the fluid velocity at some point in space. The change in velocity of a fluid element in time $dt$ is the sum of the change in velocity of the fluid at the location of the fluid element during the same time interval, and, the difference in the velocities at the starting and ending locations of the fluid element, separated by $\overrightarrow{dr}$. Thus,

$$
d\vec{v}=\frac{\partial\vec{v}}{\partial t}dt+\frac{\partial\vec{v}}{\partial x}dx+\frac{\partial\vec{v}}{\partial y}dy+\frac{\partial\vec{v}}{\partial z}dz
=\frac{\partial\vec{v}}{\partial t}dt+\left(\overrightarrow{dr}\cdot\vec{\nabla}\right)\vec{v}
$$

$$
\Rightarrow \frac{d\vec{v}}{dt}
=\frac{\partial\vec{v}}{\partial t}+\left(\vec{v}\cdot\vec{\nabla}\right)\vec{v}
$$

Using this, we get _Euler's equation_,

$$
\frac{\partial\vec{v}}{\partial t}+\left(\vec{v}\cdot\vec{\nabla}\right)\vec{v}=-\frac{1}{\rho}\vec{\nabla}p
$$

When the fluid is in a gravitational field, there is another force and Euler's equation takes the form,

$$
\frac{\partial\vec{v}}{\partial t}+\left(\vec{v}\cdot\vec{\nabla}\right)\vec{v}=-\frac{1}{\rho}\vec{\nabla}p+\vec{g}
$$

The above derivation assumes an ideal fluid in which dissipative forces are unimportant, _i.e._, there is no viscosity or thermal conductivity.

Under uniform gravitational field, if we have a fluid at rest, then, Euler's equation implies that $\vec{\nabla}p=\rho \vec{g}$. If $g=(0,0,-g)$, then, integrating, we get, $p=-\rho g z+constant$. Now, if the fluid has a free surface at a height, $z=h,$ at which the pressure is the atmospheric pressure, $p_0$, then we have, $p=p_0+\rho g(h-z)$.

## The Two Kinds of Forces in a Fluid

There are two kinds of forces which act on a fluid element.

1. Long Range Forces. This includes the gravitational force and the electrostatic force (for fluids with charge).
2. Short Range Forces / Contact Forces. This includes intermolecular forces such as van der Waals forces.

For a fluid element of volume $dV$, the long range forces act over the entire bulk of the element. For a force field for which the force per unit mass is $\vec{F}$, the force experienced by the volume element at $\vec{x}$ at time $t$ is $\vec{F}(\vec{x},t)\rho dV$.

The short range forces cannot penetrate into the bulk of the element and act along the surface only. Consider a surface element in the fluid whose area is $dA$ and with a normal vector $\hat{n}$. The force due to the short range forces on this surface element is proportional to $dA$. This force also depends on
the orientation of the surface element, _i.e._, on $\hat{n}$. Thus, we can denote the force on the surface element at $\vec{x}$ at time $t$ by $\vec{\Sigma}(\hat{n},\vec{x},t)dA$. By convention, this is the force by the fluid towards which $\hat{n}$ points on the flud on the other side of the surface element. Here $\vec{\Sigma}$ represents the local _stress_. From Newton's third law of motion, it is clear that $\vec{\Sigma}$ is an odd function of $\hat{n}$, _i.e._, $\vec{\Sigma}(-\hat{n},\vec{x},t)=-\vec{\Sigma}(\hat{n},\vec{x},t)$.

[Next (Stress Tensor)](https://saurishc.github.io/stressTensor)

[Back to syllabus](https://saurishc.github.io/fluidMechanics)
