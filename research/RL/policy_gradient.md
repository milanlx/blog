# Policy Gradient 

$$
J(\pi_{\theta}) = \underset{\tau \sim \pi_{\theta}}{\mathbb{E}} [R(\tau)] = \int_{\tau} P(\tau | \pi_{\theta}) \: R(\tau)
$$

$$
\begin{equation*}
\begin{aligned}
\nabla_{\theta} \: J(\pi_{\theta}) 
    & = \nabla_{\theta} \: \int_{\tau} P(\tau | \pi_{\theta}) \: R(\tau) \\
    & = \int_{\tau} \nabla_{\theta} \: P(\tau | \pi_{\theta}) \: R(\tau) \\
    & = \int_{\tau} P(\tau | \pi_{\theta}) \: \frac{\nabla_{\theta} P(\tau | \pi_{\theta})}{P(\tau | \pi_{\theta})} \: R(\tau) \\
    & = \underset{\tau \sim \pi_{\theta}}{\mathbb{E}} [\nabla_{\theta} \log P(\tau|\theta) \: R(\tau)] \\
    & = \underset{\tau \sim \pi_{\theta}}{\mathbb{E}} \big[ \sum_{t=0}^{T} \nabla_{\theta} \log \pi_{\theta}(a_t|s_t) \: R(\tau) \big] \\
    & = \underset{\tau \sim \pi_{\theta}}{\mathbb{E}} \big[ \sum_{t=0}^{T} \nabla_{\theta} \log \pi_{\theta}(a_t|s_t) \: \sum_{t'=t}^{T} r(t') \big] \\
    & = \frac{1}{|\mathcal{D}|} \sum_{\tau \in \mathcal{D}} \sum_{t=0}^{T} \nabla_{\theta} \log \pi_{\theta}(a_t|s_t) \: G(t)
\end{aligned}
\end{equation*}
$$
