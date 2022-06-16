---
layout: default
title: IG/ Statistical manifolds
section: ig
katex: true
---

{% include ig-back.html %}

# Statistical manifolds

Let $$(\mathcal X, \mathcal F)$$ be a measure space with a $$\sigma$$-finite measure $$\mu$$. $$L^1(\mu)$$ denotes the Banach space of $$\mu$$-integrable functions, and

$$\mathcal P(\mathcal X) = \left\{ p \in L^1(\mu) \;\middle|\; p>0, \int_{\mathcal{X}} p\, d\mu=1 \right\}$$

denotes the family of all densities of probability measures equivalent to $$\mu$$ (note: $$\mathcal P(\mathcal X)$$ is naturally a topological space with the induced $$L^1$$ topology). The expectation of a function $$f$$ with respect to some $$p$$ is $$E_p [f] \coloneqq \int_{\mathcal X} f(x) p(x) d\mu(x)$$, if it exists.

A (regular) **statistical model** parametrized by some open set $$\Theta \subset \mathbb R^d$$ is a subspace $$M \subset \mathcal P(\mathcal X)$$ together with a homeomorphism $$\Theta \to M$$ denoted by $$\theta \mapsto p_\theta$$, that satisfies the following conditions:

1. for every $$x \in \mathcal X$$, the map $$\theta \mapsto p_\theta(x)$$ is $$C^{\infty}$$,
2. let $$\ell_\theta(x) \coloneqq \log p_\theta(x)$$ and $$\partial_i \coloneqq \frac{\partial}{\partial \theta_i}$$. For every $$\theta \in \Theta$$, the set of functions $$\left\{ \partial_i \ell_\theta : i \in \{1,\dots,d\} \right\}$$ is linearly independent,
3. all partial derivatives of $$p_\theta$$ and $$\ell_\theta$$ commute with integrals, and
4. all moments $$E_\theta[\partial_{i_1} \ell_\theta \dots \partial_{i_n} \ell_\theta ]$$ exist.

If, furthermore, $$M$$ has the structure of a $$C^\infty$$ manifold completely parametrized by $$\theta$$, then $$M$$ is said to be a **statistical manifold**.

## Examples

- [Exponential families](/information-geometry/exponential-families.html)
- [Mixture families](/information-geometry/mixture-families.html)
