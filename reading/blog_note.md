
1. [AI Is A Five Layer Cake](https://blogs.nvidia.com/blog/ai-5-layer-cake/)
  - ...it helps to reason from first principles...
  - energy, chips, infrastructure, models, applications: AI workloads require enormous parallelism, high-bandwidth memory and fast interconnects. 
  - We are still early. Much of the infrastructure does not yet exist. Much of the workforce has not yet been trained. Much of the opportunity has not yet been realized. But the direction is clear.

2. [45 Thoughts About Agents](https://secondthoughts.ai/p/45-thoughts-about-agents)
  - Agents, by contrast, are traditional software, and can be updated incrementally – tweak a prompt here, add a new integration there. Model releases come months apart; Claude Code sometimes has multiple releases in one day. The ship → get feedback → improve → ship cycle for an agent can be very fast.
  - if you just naively hand pieces of work to an agent, your productivity can actually go down. It’s easy to fall into a cycle where an agent produces something for you, you provide feedback, the agent makes revisions, you check it again, ad infinitum.
  - putting the agent in a position to check its own work; have one agent do the work, and then a separate agent check the work; spell out in great detail how I’d like it to go about a task (product to prompt?)
  - I vibe-coded an app that generates summaries of all the (many!) newsletters and podcasts I follow.
  - Agents are going to progress rapidly, by any metric: usage, capabilities, impact. AI’s impact is the product of eight separate factors; pre-training, post-training, inference compute scaling, agent scaffolding, app design, user aptitude, workflow refactoring, and adoption.
  - If the current wave of agent adoption continues, API providers may have to significantly ration usage.

3. [The RL Environment Business](https://x.com/elliotarledge/status/2032753593535574433)
   - The reality of building a headless Minecraft server that runs fast enough for millions of RL rollouts, with a verifier that correctly evaluates whether the model actually achieved its objective, is a massive engineering challenge.
   - how the business probably works today: the lab identifies capability gaps -> they spec out environment requirements -> a contracting company builds the environments -> Code review and acceptance -> integration into training
   - containerized execution environments (think: sandboxed Docker containers where submitted environments run safely) that are commodity infrastructure...

4. [How To Reason About A Messy Future](https://x.com/systematicls/status/2030986094368432326)
  - When the future is genuinely noisy, when the rate of change is fast enough that most analogies break down, people tend to do one of two things. They either wait for certainty before acting, or they pattern-match to the past ("this is like the internet boom") and act on the wrong model. Both are mistakes.
  - It is worth reasoning from first principles under incomplete information. You don't need to know exactly how something plays out. You just need to be directionally correct, and you need to structure your bets so that being early and wrong is survivable, while being early and right is disproportionately rewarding.
  - By the time the signal is obvious, the trade is crowded. In markets, you pay for early conviction with uncertainty. In careers and startups, the currency is the same.
  - ... action creates information. Moving towards action is discovery.

5. [A Path Towards Autonomous Machine Intelligence](https://openreview.net/forum?id=BZ5a1r-kVsf)
  - world model, hierarchies of models with multiple levels of abstraction, self-supervised
  - module: configurator, perception, world model, cost, short-term memory, actor
  - perception-action loop: system 1 (reactive); system 2 (reasoning + planing with world model) ~ MPC

6. [2030年大预言：会用AI的人进入新贵族，不会用的人变成数字农奴](https://x.com/dashen_wang/status/2037360754274488659?s=43&t=HWl3cSGVNm08NsHl5SGiEA)
  - 新技术总是先有现象，再造词语。词语跟不上的地方，就是变化正在发生的地方。
  - 会"编排"AI完成复杂工程任务的人，2027年会变得极度稀缺。他们懂得拆解任务、设计工作流、评估AI输出质量。
  - 意图层（intent layer）：现在你用软件的方式是：打开APP，找功能，点击，填表，提交。这个交互模式统治了三十年。意图层是指一个新的范式：你只需要表达你想要什么，有一个系统帮你路由到正确的工具并执行。
  - 当越来越多的搜索和决策被AI代劳，传统广告逻辑崩塌。
  - 人类最稀缺的，将不再是执行力，而是想法的质量、判断的准确度，以及一个至今仍被严重低估的能力：知道什么时候不该信任AI的结论。
  - 新职业：AI编排师；上下文架构师；Skill开发者
  - 自己的知识库：当所有人都用同一个基础模型，你积累的私有数据和结构化经验，是让你的AI比别人的AI更聪明的唯一方法。

7. [范式转换不是旧框架的修修补补，而是整个世界观的更替（内含书单）](https://x.com/pandatalk8/status/2036404404388241423?s=43&t=HWl3cSGVNm08NsHl5SGiEA)
  - 正在形成的新秩序: "被雇佣"到"被连接"；"积累知识"到"驾驭工具"；"规模经济"到"个体经济"；"确定性追求"到"反脆弱设计"；"物质占有"到"体验和连接"
  - 稳定期的最优策略是优化——在既有规则内做到最好；转型期的最优策略是探索——用最小的成本，尝试最多的可能性，快速找到适合自己的方向。
