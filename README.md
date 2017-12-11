# Multi-Agent Reinforcement Learning project (MARL)

## MARL Lunar Lander environment
The original GYM environment was modified for 2 Lunar landers (continuous). The trick is how to evaluate the reward between 2 agents. The previous one was simply adding 2 rewards; however this yields higher payout such that the model was stuck in a local minimum.

We modified the reward system to take considerations when 2 agent were receiving 2 scores (1 big positive and 1 small negative): in new reward system this will be forced to be 0 while in old system this was positive.

## Our model
We modified the existing [codes](https://github.com/NVlabs/GA3C) of hybrid CPU/GPU version of the A3C algorithm and adapted it to multi-agent decentralized actor and centralized critic approach according this [paper](https://arxiv.org/pdf/1706.02275.pdf).

## Results
Comparison between models and reward systems:

[[plots_for_report/actor_reward_comparison.pdf]]

Comparison between hyper-parameters:

[[plots_for_report/lambda_beta_comparison.pdf]]

Comparison between number of hidden units:

[[plots_for_report/neurons_comparison.pdf]]

## Future work - Gathering (discrete action space)
We could expand our work for competitive and discrete environment such as Gathering. See more details in branch [gathering](https://github.com/osipychev/IE598_RL/tree/gathering).
