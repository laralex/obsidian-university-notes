---
aliases: [SDE, Stochastic continuous-time system]
---

> **Stochastic [[CT]] system** - is described with stochastic differential equations (SDEs)
> [[State transition law]] $dX_t = f(X_t, U_t)dt + \sigma(X_t, U_t)dB_t$
> For simpliticy:
> [[Output map]]  $Y_t = h(X_t, U_t)$
> [[Markov policy]] $U_t = \kappa(X_t)$

$f(X_t, U_t)$ is also called [[Drift function]]

$\sigma(X_t, U_t)$ is also called [[Diffusion function]]

Such systems have ==issues== with *strong* solution existance

Example - Black-Scholes model of stock trading:
*  risk free asset with rate of return $r$
$$dS_t = r S_t dt$$
* risky asset, with mean rate of return $\mu$ and volatility $\sigma$
$$dR_t = \mu R_t dt + \sigma dB_t$$
* Stochastic [[State x]]: $X = X^S + X^R$ wealth of assets
* Define [[Policy k|Policy]] as $$U_t = (\Pi_t, C_t)^T$$ where $\Pi_t = X^R_t/X_t$ is a sub-action of investment into risky assets, and $C_t$ is a sub-action of money consumption
* Then [[State transition law]] (progression of wealth):
$$dX_t = (r X_t + (\mu-r)\Pi_t X_t - C_t )dt + \sigma \Pi_t X_t dB_t$$
starting from initial non-stochastic state $x_0$ such that $$\mathbb{P}(X_0 = x_0) = 1$$

A [[Stochastic CT system]] can be even more complex, by introducing ==partial derivatives==, (thus turning it into stochastic partial differential equations (PDEs)