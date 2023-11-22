---
layout: post
title: "Fluid properties"
author: "Saurish Chakrabarty"
categories: journal
tags: [documentation,sample]
---

### Equation of state
For a given mass of fluid in thermodynamic equilibrium, the state is uniquely specified by the values of two parameters, _e.g._, the pressure and the temperature. Thus, there exists a relation connecting the pressure, the temperature and the density. 
$$
f(p,\rho,T)=0.
$$
Such a relation is known as the _equation of state_ of the fluid. Often, the function $f$ exists but is not known in closed form. In simple idealized situations, the above relation may take the form of the ideal gas equation of state or the van der Waals' equation of state. Approximate equations of state, valid in a limited region in parameter space, are often written down.

## Transport phenomena
It is common to find a fluid that is not in thermodynamic equilibrium. Different regions of the fluid have different properties. In such a situation, the fluid has a tendency to approach an equilibrium state by exchanging mechanical or thermal properties across diffrent regions of the fluid as long as there is inhomogeneity. _Transport phenomena_ refers to processes which lead to exchange of a quantity (which satisfies some conservation law) among two elements of a fluid where this quantity has different values.
- Diffusion: If the composition of a fluid varies in space, then there is a non-zero flux of matter across any elementary surface in a direction that lowers the inhomogeneity.
- Thermal conduction: If the temperature of different regions of a fluid are different, then heat flows across any elementary surface from its hotter to its colder side.
- Viscosity: If the continuum velocity in a fluid is non-uniform, then there are non-zero shear stresses in different regions of the fluid. For an elementary surface across which the fluid velocity is different on its two sides, a shear stress is developed so as to reduce the velocity difference.

## Linear Relation between the Flux and the Gradient of a Scalar Intensity
Let us assume that for the transport phenomenon we study, the relevant intensity is denoted by a scalar quantity, $C$. This could be the local concentration or the local temperature. The objective of transport processes is to nullify the spatial inhomogeneity in $C$. If the flux of the quantity associated with $C$ is denoted by $\vec{f}(\vec{x},t)$, then the net flow of this quantity per unit time across a surface element, $\overrightarrow{dA}=dA\hat{n}$, is given by $\vec{f}\cdot\overrightarrow{dA}$. If the variation in $C$ is gradual (not too rapidly varying in space), then there is a linear relation between $\vec{f}$ and the gradient of $C$. This assumption of gradual variation can be quantitatively written as,
$$
\frac{\frac{\partial C}{\partial x}}{\frac{\partial^2 C}{\partial x^2}}\gg\text{(typical length scales of particle motion or interaction)}
$$


