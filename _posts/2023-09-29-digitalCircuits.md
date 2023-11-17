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
- **OR(+)**: $X+Y=0$ if both $X$ and $Y$ are 0, and 1 otherwise.
- **AND($\cdot$)**: $X\cdot Y=1$ if both $X$ and $Y$ are 1, and 0 otherwise. The dot sign is often skipped.

All these operations satisfy the closure property, _i.e._, the result is also a Boolean variable. This means that the output can be used as an input for another operation.

**Operator precedence**: Like in usual algebra, where we have the BODMAS rule, here too expressions inside brackets are simplified first, followed by AND operations and finally OR.

### Some Basic Identities

1. $\overline{\overline{A}}=A$
2. $A+0=A$ (0 is the additive identity)
3. $A\cdot 1=A$ (1 is the multiplicative identity)
4. $A+1=1$
5. $A\cdot 0=0$
6. $A+A=A\cdot A=A$
7. $A+\overline{A}=1$
8. $A\cdot\overline{A}=0$
9. $A+B=B+A$ (addition is commutative)
10. $AB=BA$ (multiplication is commutative)
11. $A+(B+C)=(A+B)+C$ (addition is associative)
12. $A(BC)=(AB)C$ (multiplication is associative)
13. $A(B+C)=AB+AC$ (multiplication is distributive over addition)
14. $A+BC=(A+B)(A+C)$ (addition is distributive over multiplication -- not true in ordinary algebra)
15. $\overline{A+B}=\overline{A}\cdot\overline{B}$ (first de Morgan's Law)
16. $\overline{AB}=\overline{A}+\overline{B}$ (second de Morgan's Law)

Each of these identities can be proved by constructing corresponding truth tables. _E.g._, proof for $A+AB=A$ is established using the following truth table.

|$A$|$B$|$AB$|$A+AB$|
|---|---|---|---|
|0|0|0|0|
|0|1|0|0|
|1|0|0|1|
|1|1|1|1|
|---|---|---|---|

The first and fourth columns are identical. Hence, $A+AB=A$.

