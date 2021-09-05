---
aliases: [DT, Discrete-time deterministic system]
---

> Discrete-time deterministic (DT) - a simplest example of a [[System]]
>- [[State transition law]] is explicitly computed 
>$$x_{k+1} = f(x_k, u)$$
>- [[Output map]] is explicitly computed 
>$$y_k = h(x_k, u)$$
>- [[Policy k]] is explicitly computed
$$u = \kappa(x_k)$$
>- [[State x|State space]], [[Output y|Output space]], [[Input u|Aciton space]] are real vectors

Examples:
- digital device
- digital filter
- population dynamics
$$x_{k+1} = x_k + (born_k  - died_k) + (immigrants_k - emmigrants_k)$$
#SEMINAR-1 What can be a [[Controller]] here?