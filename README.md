# Multi-Agent Reinforcement Learning project (MARL)

## MARL Lunar Lander environment
The original OpenAI GYM environment was modified for 2 Lunar landers (continuous). The trick is how to evaluate the reward between 2 agents. The previous one was simply adding 2 rewards; however this yields higher payout such that the model was stuck in a local minimum.

![fail](https://github.com/Yizhi-Fang/IE598_RL/blob/master/plots_for_report/fail.gif)

We modified the reward system to take considerations when 2 agent were receiving 2 scores (1 big positive and 1 small negative): in new reward system this will be forced to be 0 while in old system this was positive.

## Our model
We modified the existing [codes](https://github.com/NVlabs/GA3C) of hybrid CPU/GPU version of the A3C algorithm and adapted it to multi-agent decentralized actor and centralized critic approach according this [paper](https://arxiv.org/pdf/1706.02275.pdf).

## Results
Comparison between models and reward systems:

![plot1](https://github.com/Yizhi-Fang/IE598_RL/blob/master/plots_for_report/actor_reward_comparison.png)

Comparison between hyper-parameters:

![plot2](https://github.com/Yizhi-Fang/IE598_RL/blob/master/plots_for_report/lambda_beta_comparison.png)

Comparison between number of hidden units:

![plot3](https://github.com/Yizhi-Fang/IE598_RL/blob/master/plots_for_report/neurons_comparison.png)

Fiannlly, our best model with tunned hyper-parameters successfully trains the 2 agents

![success](https://github.com/Yizhi-Fang/IE598_RL/blob/master/plots_for_report/success.gif)

## Future work - Gathering (discrete action space)
We could expand our work for competitive and discrete environment such as Gathering. See more details in branch [gathering](https://github.com/osipychev/IE598_RL/tree/gathering).
