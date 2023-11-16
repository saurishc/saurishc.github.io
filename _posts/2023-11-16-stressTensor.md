---
layout: post
title: "The Stress Tensor"
author: "Saurish Chakrabarty"
categories: journal
tags: [documentation,sample]
---

Consider a tetrahedral volume element as shown in the figure below. It has three orthogonal faces areas $dA_1$, $dA_2$, and $dA_3$, and with normals $\hat{a}$, $\hat{c}$ and $\hat{g}$, respectively. (The symbols for the unit normals were chosen because I could not find a quick and easy way to write $\hat{b}$ while creating this figure. You can call them $\hat{a}$, $\hat{b}$ and $\hat{c}$ as is done in Batchelor's book.)

![Alt text](https://saurishc.github.io/images/orthogonalTetrahedron.png "Tetrahedral volume element with three orthogonal faces")

The fourth face has an area $dA$ and a normal $\hat{n}$ pointing out of the volume element. For the orthogonal faces, the outward normals are in directions, $-\hat{a}$, $-\hat{c}$ and $-\hat{g}$, respectively. The sum of the surface forces on the fluid element is therefore given by,
$$\vec{\Sigma}(\hat{n})dA+\vec{\Sigma}(-\hat{a})dA_1+\vec{\Sigma}(-\hat{c})dA_2+\vec{\Sigma}(-\hat{g})dA_3\\
=
\vec{\Sigma}(\hat{n})dA-\vec{\Sigma}(\hat{a})dA_1-\vec{\Sigma}(\hat{c})dA_2-\vec{\Sigma}(\hat{g})dA_3.$$

It is clear that $dA_1$ is the projection of $dA\hat{n}$ on $\hat{a}$. Therefore, $dA_1=dA\hat{n}\cdot\hat{a}$. Similarly, $dA_2=dA\hat{n}\cdot\hat{c}$ and $dA_3=dA\hat{n}\cdot\hat{g}$.  Thus, the sum of the surface forces on the fluid element can be simplified to,

$$
\left(\vec{\Sigma}(\hat{n})
-\vec{\Sigma}(\hat{a})\hat{a}\cdot\hat{n}
-\vec{\Sigma}(\hat{c})\hat{c}\cdot\hat{n}
-\vec{\Sigma}(\hat{g})\hat{g}\cdot\hat{n}
\right)dA
$$

Now, for the volume element, writing Newton's second law, we get,
$$
\rho dV\times \text{acceleration}
=
(\text{sum of bulk forces})+(\text{sum of surface forces})
$$

The sum of bulk forces is proportional to $dV$ but the sum of surface forces is proportional to $dA$. As the volume element is made arbitrarily small, we get an inconsistency, _i.e._, the left hand side of this equation become negligible compared to the sum of surface forces. This means that the net surface force must vanish. Thus, we get,

$$
\vec{\Sigma}(\hat{n})
=\vec{\Sigma}(\hat{a})\hat{a}\cdot\hat{n}
+\vec{\Sigma}(\hat{c})\hat{c}\cdot\hat{n}
+\vec{\Sigma}(\hat{g})\hat{g}\cdot\hat{n}
$$

The $i$\textsuperscript{th} component of $\vec{\Sigma}$ is therefore given by,

$$
\Sigma_i(\hat{n})
=\left(
\Sigma_i(\hat{a})a_j
+\Sigma_i(\hat{c})c_j
+\Sigma_i(\hat{g})g_j
\right)n_j
$$

where we have also expanded the dot products and used Einstein's summation convention.

[Back to syllabus](https://saurishc.github.io/fluidMechanics)
