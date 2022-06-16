---
layout: default
title: IG/ Dually flat manifolds
katex: true
---

[[↑Information Geometry]](/information-geometry)

# Dually flat manifolds

Let $$(M,g,\nabla,\nabla^*)$$ be a [dually connected](/information-geometry/dual-connections.html) Riemannian manifold. It will be called a **dually flat manifold** if $$\nabla$$ is flat (and consequentially $$\nabla^*$$ too).

If $$M$$ is dually flat, then there exists locally two affine coordinate systems $$\theta=(\theta^1,\dots,\theta^n)$$ and $$\eta=(\eta_1,\dots,\eta_n)$$ for $$\nabla$$ and $$\nabla^*$$ respectively, with local basis $$\partial_i \coloneqq \frac{\partial}{\partial \theta^i}$$ and $$\partial^j \coloneqq \frac{\partial}{\partial \eta_j}$$, which are affine in the sense that $$\nabla_{\partial_i} \partial_j \equiv 0$$ and $$\nabla^*_{\partial^i} \partial^j \equiv 0$$. In other words, $$\theta$$ vanishes the Christoffel symbols of $$\nabla$$ and $$\eta$$ vanishes the Christoffel symbols of $$\nabla^*$$.

In the case where $$\nabla$$ and $$\nabla^*$$ are duals, we can construct such coordinate systems $$\theta$$ and $$\eta$$ with the additional property that their local frames are duals:

$$ \langle \partial_i, \partial^j \rangle = \langle \partial^i, \partial_j \rangle = \delta_{ij}.$$

Such coordinate systems are called **dual coordinate systems** for $$(M,g,\nabla,\nabla^*)$$.
