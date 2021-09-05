---
aliases: [Accumulated instantaneous objective, Expected instantaneous objective, Discounted instantaneous objective, Cost-to-go]
---

> **Objective** - a cumulative value of [[Instantaneous objective]] function.
> Notated as $J(x_0,\kappa)$ for some [[Policy k|Policy]] and a starting [[State x]]. 

In an [[Horizon|Infinite horizon]] setting the [[Objective]] doesn't depend on anything else but  $x_0$ and $\kappa$

#SEMINAR-1 Why doesn't it depend on time or anything else?

In practice it's computed with a discounting factor $\gamma \in [0, 1]$, that controls a decay of long-term [[Input u|Control]] importance.

[[DT system\|DT]] $$\sum_{k=0}^{\infty}\gamma^k \rho(x_k, u_k)$$|[[MDP system\|MDP]] $$\mathbb{E}_{X_k, U_k} \left[ \sum_{k=0}^{\infty}\gamma^k \rho(X_k, U_k) \right]$$
--:|:--
**[[CT system\|CT]]** $$\int_{0}^{\infty} e^{-\gamma t} \rho(x(t), u(t))dt$$|**[[Stochastic CT system\|SDE]]**$$\mathbb{E}_{X_k, U_k} \left[ \int_{0}^{\infty} e^{-\gamma t} \rho(X_t, U_t)dt \right]$$
