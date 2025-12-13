# Policy Gradient 

$$
J(\pi_{\theta}) = \underset{\tau \sim \pi_{\theta}}{\mathbb{E}} [R(\tau)] = \int_{\tau} P(\tau | \pi_{\theta}) \: R(\tau)
$$

$$
\begin{equation*}
\begin{aligned}
\nabla_{\theta} \\: J(\pi_{\theta}) 
    & = \nabla_{\theta} \\: \int_{\tau} P(\tau | \pi_{\theta}) \\: R(\tau) \\
    & = \int_{\tau} \nabla_{\theta} \\: P(\tau | \pi_{\theta}) \\: R(\tau) \\
    & = \int_{\tau} P(\tau | \pi_{\theta}) \\: \frac{\nabla_{\theta} P(\tau | \pi_{\theta})}{P(\tau | \pi_{\theta})} \\: R(\tau) \\
    & = \underset{\tau \sim \pi_{\theta}}{\mathbb{E}} [\nabla_{\theta} \log P(\tau|\theta) \\: R(\tau)] \\
    & = \underset{\tau \sim \pi_{\theta}}{\mathbb{E}} \big[ \sum_{t=0}^{T} \nabla_{\theta} \log \pi_{\theta}(a_t|s_t) \\: R(\tau) \big] \\
    & = \underset{\tau \sim \pi_{\theta}}{\mathbb{E}} \big[ \sum_{t=0}^{T} \nabla_{\theta} \log \pi_{\theta}(a_t|s_t) \\: \sum_{t\prime=t}^{T} r(t\prime) \big] \\
    & = \frac{1}{|\mathcal{D}|} \sum_{\tau \in \mathcal{D}} \sum_{t=0}^{T} \nabla_{\theta} \log \pi_{\theta}(a_t|s_t) \\: G(t)
\end{aligned}
\end{equation*}
$$


```python
import torch
import torch.nn.functional as F
import gymnasium as gym


class DiscreteEnv:
    def __init__(self, env_name, env_num): 
        self.envs = [gym.make(env_name) for i in range(env_num)]
        self.action_space = self.envs[0].action_space.n
        self.observation_space = self.envs[0].observation_space.shape[0]
    
    def rollout(self, policy, mode): 
        trajectories = []
        for env in self.envs:
            states, actions, rewards = [], [], []
            observation, info = env.reset()
            terminated, truncated = False, False
            while not (terminated or truncated):
                states.append(observation)

                action = policy.get_action(torch.tensor(observation), mode)
                observation, reward, terminated, truncated, info = env.step(action)
                actions.append(action)
                rewards.append(reward)
            reward_to_go = convert_reward_to_go(rewards)
            trajectories.append([states, actions, reward_to_go])
        
        return trajectories
```
