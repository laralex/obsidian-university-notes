---
aliases: [MDP, Markov decision process]
---

> **Markov decision process (MDP)** - probabalistic version of [[DT system]]
> - Next [[State x]] is seen as a random variable $X_{k+1}$, with value drawn from a PDF[^1], conditioned on current [[State x]] and [[Input u|Action u]] 
> $$X_{k+1} \sim P_X(x_{k+1}|x_k,u_k)$$
> - [[Input u|Action u]] is seen as a random variable $U_{k}$, with value drawn from a PDF, conditioned on current state ^[$\Theta$ is set of parameters of [[Policy k]] subject to optimization]
> $$U_{k} \sim P^{\Theta}_U(u_{k+1}|x_k)$$

Examples:
- turned-based game with RNG
- chat-bot
- stock market

### Practical Gaussian MDP
> $$X_{k+1} \sim \mathcal{N}(f(X_{k}, U_{k}), \Sigma_\mathcal{W})$$
> $$U_{k} \sim \mathcal{N}(\mathcal{K}^{\Theta}(X_{k}), \Sigma_U)$$
> where $f$, $\mathcal{K}^{\Theta}$ are definite functions

==Informal interpretation:== $x_{k+1}$ is on average a definite value $f(x_k, u_k)$ plus additive Gaussian noise $w_k$ with covariance $\Sigma_\mathcal{W}$

#SEMINAR-1 What kind of [[System]] does ==chess== belong to? Describe it. Consider another player as a source of [[Disturbance w]]

### Notation interpretation
Often [[State x|State space]] or [[Input u|Action space]] is discrete, and the notation of PDF can be seen as just a ==specific probability==, e.g.
$$P_X(x_{k+1}|x_k,u_k) = \mathbb{P}(X_{k+1} = x_{k+1} | X_{k} = x_k, U_k = u_k)$$

Remember that if the spaces are continuous the probability is obtained by computing integrals over some vicinity of states

[^1]: Also called [[Transition PDF]]