---
layout: ig
title: IG/ Normal family (univariate)
section: ig
katex: true
---

# Normal family (univariate)

- **Probability density:**

$$f_{\mu, \sigma} (x) = \frac{1}{\sqrt{2\pi} \sigma} \exp\left( \frac{- (x-\mu)^2}{2 \sigma^2} \right),\; x \in \mathbb{R}.$$

- **Usual parameters:** $$\mu \in \mathbb{R}$$ (mean), $$\sigma > 0$$ (standard deviation)


## 1. Fisher geometry
- **Fisher information metric:**

$$G(\mu,\sigma) = \begin{bmatrix} \frac{1}{\sigma^2} & 0 \\ 0 & \frac{2}{\sigma^2} \end{bmatrix}$$

- **$$\alpha$$-Christoffel symbols:**

    $$\begin{align*}
    &\Gamma_{11}^{2\, (\alpha)} = \frac{1-\alpha}{2\sigma},\quad
    \Gamma_{12}^{1\, (\alpha)} = \Gamma_{21}^{1\, (\alpha)} = \frac{1+\alpha}{\sigma},\quad
    \Gamma_{22}^{2\, (\alpha)} = -\frac{1+2\alpha}{\sigma},\\
    &\Gamma_{11}^{1\, (\alpha)} = \Gamma_{12}^{2\, (\alpha)} = \Gamma_{21}^{2\, (\alpha)} = \Gamma_{22}^{1\, (\alpha)} = 0.
    \end{align*}$$

- **$$\alpha$$-curvature:** constant, $$\kappa = -\frac{1}{2}(1 - \alpha^2)\;$$ (<a href="/information-geometry/dually-flat.html">dually flat</a> for $$\alpha= \pm 1$$)
- **Fisher-Rao distance:**
    - Fixed mean: $$d ( (\mu, \sigma_1), (\mu, \sigma_2) ) = \sqrt{2} \left\vert\log\frac{\sigma_2}{\sigma_1}\right\vert$$
    - Fixed variance: $$d ( (\mu_1, \sigma), (\mu_2, \sigma) )
    =
    \sqrt{2} \log \frac{
        4 \sigma^2 + (\mu_1 - \mu_2)^2 + |\mu_1 - \mu_2| \sqrt{8\sigma^2 + (\mu_1-\mu_2)^2}
    }{4\sigma^2}
    $$.

    - General:

    $$\begin{align*}
        d ( (\mu_1, \sigma_1), (\mu_2, \sigma_2) )
        &=
        \sqrt{2} \log\frac{
            \left| \left( \frac{\mu_1}{\sqrt{2}}, \sigma_1 \right) - \left( \frac{\mu_2}{\sqrt{2}}, -\sigma_2 \right)\right|
            +
            \left| \left( \frac{\mu_1}{\sqrt{2}}, \sigma_1 \right) - \left( \frac{\mu_2}{\sqrt{2}}, \sigma_2 \right)\right|
        }{
            \left| \left( \frac{\mu_1}{\sqrt{2}}, \sigma_1 \right) - \left( \frac{\mu_2}{\sqrt{2}}, -\sigma_2 \right)\right|
            -
            \left| \left( \frac{\mu_1}{\sqrt{2}}, \sigma_1 \right) - \left( \frac{\mu_2}{\sqrt{2}}, \sigma_2 \right)\right|
        }\\
        &=
        \sqrt{2}\log\frac{
            \mathcal{F}((\mu_1,\sigma_1), (\mu_2, \sigma_2)) + (\mu_1 - \mu_2)^2 + 2(\sigma_1^2 + \sigma_2^2)
        }{4 \sigma_1 \sigma_2},
    \end{align*}$$
    
    where $$\mathcal{F}((\mu_1,\sigma_1), (\mu_2, \sigma_2)) = \sqrt{ \left( (\mu_1 - \mu_2)^2 + 2(\sigma_1 - \sigma_2)^2 \right)\left( (\mu_1 - \mu_2)^2 + 2(\sigma_1 + \sigma_2)^2 \right) }$$.


## 2. Information theory
- **Entropy:** $$H = \frac{1}{2} \log \left( 2 \pi e \sigma^2 \right)$$
- **Kullback-Leibler divergence:**

$$D_\mathrm{KL} ( f_{\mu_1, \sigma_1} \| f_{\mu_2, \sigma_2} ) = \log\left(\frac{\sigma_2}{\sigma_1}\right) + \frac{1}{2} \left( \frac{\sigma_1^2}{\sigma_2^2} + \frac{(\mu_1 - \mu_2)^2}{\sigma_2^2} - 1  \right).$$


## 3. As exponential manifold
- **Natural parameters:** $$\displaystyle\theta_1 = \frac{\mu}{\sigma^2} \in \mathbb{R},\quad \theta_2 = \frac{-1}{2 \sigma^2} < 0$$
- **Potential (log-normalizer):**

$$\varphi(\theta_1, \theta_2) = - \frac{\theta_1^2}{4 \theta_2} + \frac{1}{2}\log\left( \frac{-\pi}{\theta_2} \right)$$

- **Sufficient statistic:** $$t_1(x) = x,\quad t_2(x) = x^2$$
- **Dual parameters:** $$\eta_1 = \mu \in \mathbb R$$ (first moment), $$\eta_2 = \mu^2 + \sigma^2$$ (second moment)
<!-- - **Dual potential:** $$\psi(\eta_1, \eta_2) = $$ -->


## 4. As homogeneous manifold / Lie group
- Denote the parameter space by $$\mathcal{N} = \left\{ (\mu,\sigma) \in \mathbb{R} \times \mathbb{R}_+ \right\}$$.
- $$\mathcal{N}$$ corresponds to a (affine) Lie group with semidirect product

$$(\tilde\mu, \tilde\sigma) \cdot (\mu, \sigma) = (\tilde\sigma \mu + \tilde\mu, \tilde\sigma \sigma).$$

- The product is
    - **isometric** in the Fisher geometry,
    - **affine** with respect to $$\nabla^\alpha$$ for every $$\alpha$$.
- This left-product with $$(\tilde\mu,\tilde\sigma)$$ corresponds to reparametrization of the sample space by $$y = \frac{x-\tilde\mu}{\tilde\sigma}$$.

---

### Sources
1. S. I.R. Costa, S. A. Santos, J. E. Strapasson. [*Fisher information distance: A geometrical reading*](https://www.sciencedirect.com/science/article/pii/S0166218X14004211)
2. S. Amari, H. Nagoka. [*Methods of Information Geometry*](https://books.google.com.br/books/about/Methods_of_Information_Geometry.html?id=vc2FWSo7wLUC)
3. O. Calin, C. Udrişte. [*Geometric Modeling in Probability and Statistics*](https://www.springer.com/gp/book/9783319077789)
