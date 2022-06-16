---
layout: default
title: IG/ Dual connections
katex: true
---

[[↑Information Geometry]](/information-geometry)

# Dual connections

Let $$(M,g)$$ be a Riemannian manifold, and $$\nabla$$ be an any affine connection. The **dual connection** of $$\nabla$$ with respect to $$g$$ is a connection $$\nabla^*$$ such that

$$X \langle Y,Z \rangle = \langle \nabla_X Y,Z \rangle + \langle Y, \nabla^*_X Z \rangle$$

for $$X,Y,Z$$ vector fields.

The quadruple $$(M,g,\nabla,\nabla^*)$$ is called a **dually connected manifold**, and the triple $$(g,\nabla,\nabla^*)$$ is called a **dualistic structure** for $$M$$.

## Properties
1. The dual is unique.
2. $$\nabla^{**} = \nabla$$.
3. $$\overline\nabla = \frac{1}{2} (\nabla+\nabla^*)$$ is a metric connection. In particular, if $$\nabla,\nabla^*$$ are torsion-free, it is the Levi-Civita connection.
4. Let $$\nabla$$ be torsion-free. Then $$\nabla^*$$ is torsion-free iff $$\nabla g$$ is symmetric.
5. If $$X,Y \in T_p M$$ and $$\Pi_\gamma, \Pi^*_\gamma$$ denote parallel transport along a curve $$\gamma$$, with respect to $$\nabla$$ and $$\nabla^*$$ respectively, then $$\langle X,Y \rangle_p = \langle \Pi_\gamma X, \Pi^*_\gamma Y \rangle_q$$
6. Dual Riemann curvature tensors satisfy $$\langle R(X,Y)Z, W \rangle = - \langle R^* (X,Y)W, Z \rangle$$.
7. (Important!) $$\nabla$$ is flat iff $$\nabla^*$$ is flat.

## Examples

**<u>Example 1</u>.** Let $$\nabla^g$$ be the Levi-Civita connection of $$(M,g)$$, and $$A$$ be any symmetric 3-tensor. The following expression defines a torsion-free affine connection $$\nabla^A$$:

$$\langle \nabla^A_X Y,Z \rangle = \langle \nabla^g_X Y,Z \rangle + A(X,Y,Z),$$

The dual is given by $$(\nabla^A)^* = \nabla^{-A}$$.

**<u>Example 2</u> ($$\alpha$$-connections).** Given two fixed torsion-free dual connections $$(\nabla,\nabla^*)$$, they can be extended to a family of $$\alpha$$-connections

$$\nabla^{(\alpha)} = \frac{1+\alpha}{2}\nabla + \frac{1-\alpha}{2}\nabla^*,$$

such that $$\nabla^{(\alpha)}$$ and $$\nabla^{(-\alpha)}$$ are duals, $$\nabla^{(0)}$$, is the Levi-Civita connection, $$\nabla^{(1)} = \nabla$$ and $$\nabla^{(-1)}=\nabla^*$$. In particular, if we define the _Amari-Chentsov tensor_ as $$C(X,Y,Z) = \langle \nabla_X Y - \nabla^*_X Y,Z \rangle = \nabla g$$, then we can construct $$\nabla^{(\alpha)}$$ using the previous example for $$A= \frac{\alpha}{2}C$$.

An important case of a dualistic structure in information geometry is the pair of [exponential and mixture connections](/information-geometry/e-m-connections.html).

**See also:** [Dually flat manifolds](/information-geometry/dually-flat.html)
