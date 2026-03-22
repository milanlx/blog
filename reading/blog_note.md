
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
