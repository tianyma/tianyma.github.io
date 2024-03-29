---
layout: article
title: "Paper reading: Learning to reinforcement learn"
date: 2021-06-01
tags: paper meta-RL
mathjax: true
key: 2021-06-01-blog

weight: 0
---
## 核心思想
本文提出了一种深度元强化学习(deep meta-reinforcement learning)方法，通过强化学习训练一个循环神经网络(RNN)，使得该RNN可以通过自适应更新的方法快速适应不同任务，从而提高训练效率。
## 实现过程
本文使用A2C(Advantage Actor-Critic)算法在一系列输入任务上训练一个RNN。以MDPs(Markov Decision Processes)为例，设$\mathcal{D}$是一个MDPs分布，每个新的episode开始时，先从D采样的一个任务$m \backsim \mathcal{D}$，RNN的内部循环单元的参数会被重置，然后和环境交互一定的时长，每一次策略都是基于到目前的所有历史信息（状态，动作，奖励），agent的目标是在所有任务上最大化总的奖励。

训练结束后，网络权重会被固定，然后在一组来自$\mathcal{D}$（或者对分布$\mathcal{D}$稍微修改）的MDPs上测试agent的适应能力。
## 测试任务
本文分布在4个bandit problem和2个MDP任务上进行了测试，MDP任务分别是一个改编的[two step task](https://scienceofbehaviorchange.org/measures/two-stage-task/)和一个改编的Harlow task，最后讨论了在一个3D迷宫任务(来自deepmind lab)上进行深度元学习的方法。
## 创新点
本文是基于模型的元强化学习算法的一次尝试，通过将带LSTM的RNN用强化学习算法进行训练，可以使agent获得一定的学习适应能力。
## 算法评价


[返回文章列表]({{ site.url}}/2021/05/29/meta-reinforcement-learning.html)