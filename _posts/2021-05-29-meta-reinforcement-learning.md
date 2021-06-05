---
layout: article
title: "Paper review: meta-reinforcement-learning"
date: 2021-05-29
tags: paper review
mathjax: true
key: 2021-05-29-blog
---
## Challenges of meta-RL
- design a set of tasks that are interrelated
- find the inter-representation
- fast adaptation to new tasks 
## Papers
### environment
#### Meta-World: A Benchmark and Evaluation for Multi-Task and Meta Reinforcement Learning
- source: PMLR 2020
- method: None
- environment:
  - object manipulation 
- paper link: [http://proceedings.mlr.press/v100/yu20a/yu20a.pdf](http://proceedings.mlr.press/v100/yu20a/yu20a.pdf)
- code:  [https://github.com/rlworkgroup/metaworld](https://github.com/rlworkgroup/metaworld)
- interpretation: 
  - [https://meta-world.github.io/](https://meta-world.github.io/)

### model-based meta-RL
#### [Learning to reinforcement learn]({{ site.url }}/2021/06/01/Learning-to-reinforcement-learn.html)
- source: CogSci 2017
- method: deep meta-RL
- environment:
  - bandit problem
  - Two-step task
  - Harlow experiment 
  - 3D navigation (Deepmind Lab)
- paper link: [https://arxiv.org/pdf/1611.05763.pdf](https://arxiv.org/pdf/1611.05763.pdf)
- code:  
  - [https://github.com/Phu-archive/Learning2RL](https://github.com/Phu-archive/Learning2RL)
- interpretation: 

#### [RL^2: Fast Reinforcement Learning via Slow Reinforcement Learning]({{ site.url }}/2021/06/02/RL2.html)
- source: ICLR 2017
- method: $RL^2$
- environment:
  - multi-armed bandit problem
  - tabular MDP
  - 3D navigation (ViZDoom)
- paper link: [https://arxiv.org/pdf/1611.02779.pdf](https://arxiv.org/pdf/1611.02779.pdf)
- code:  
  - [https://github.com/mwufi/meta-rl-bandits (pytorch)](https://github.com/mwufi/meta-rl-bandits)
  - [https://github.com/VashishtMadhavan/rl2 (tensorflow)](https://github.com/VashishtMadhavan/rl2)
- interpretation: 
  - [https://zhuanlan.zhihu.com/p/32606591](https://zhuanlan.zhihu.com/p/32606591)
  - [https://openreview.net/forum?id=HkLXCE9lx](https://openreview.net/forum?id=HkLXCE9lx)

#### Prefrontal cortex as a meta-reinforcement learning system
- source: Nature Neuroscience 2018
- method: 
- environment:
- paper link: [https://www.nature.com/articles/s41593-018-0147-8](https://www.nature.com/articles/s41593-018-0147-8)
- code:  
- interpretation: 

#### A Simple Neural Attentive Meta-Learner
- source: ICLR 2018
- method: SNAIL (simple neural attentive learner)
- environment:
  - navigation 
  - robotic locomotion
- paper link: [https://openreview.net/pdf?id=B1DmUzWAW](https://openreview.net/pdf?id=B1DmUzWAW)
- code: [https://github.com/eambutu/snail-pytorch](https://github.com/eambutu/snail-pytorch)
- interpretation: 
  - [https://www.carsi.edu.cn/index_zh.htm](https://www.carsi.edu.cn/index_zh.htm)

#### PixelSNAIL: An Improved Autoregressive Generative Model
- source: ICML 2018
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/1712.09763v1.pdf](https://arxiv.org/pdf/1712.09763v1.pdf) 
- code:  
  - [https://github.com/neocxi/pixelsnail-public](https://github.com/neocxi/pixelsnail-public)
- interpretation: 

#### Concurrent Meta Reinforcement Learning 
- source: arXiv:1903.02710 preprint
- method: CMRL
- environment:
  - N-Monty-Hall
  - N-Color-Choice
  - N-Reacher (Reacher-V2 from gym)
- paper link: [https://arxiv.org/pdf/1903.02710v1.pdf](https://arxiv.org/pdf/1903.02710v1.pdf)
- code:  
- interpretation: 

#### Reinforcement Learning, Fast and Slow
- source: Trends in Cognitive Sciences 2019
- method: 
- environment:
- paper link: [https://www.cell.com/trends/cognitive-sciences/fulltext/S1364-66131930061-0](https://www.cell.com/trends/cognitive-sciences/fulltext/S1364-66131930061-0)
- code:  
- interpretation: 

#### Improving Generalization in Meta Reinforcement Learning using Learned Objectives
- source: ICLR 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/1910.04098.pdf](https://arxiv.org/pdf/1910.04098.pdf)
- code: [https://github.com/louiskirsch/metagenrl](https://github.com/louiskirsch/metagenrl) 
- interpretation: 

#### Discovering Reinforcement Learning Algorithms
- source:	arXiv:2007.08794 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2007.08794](https://arxiv.org/pdf/2007.08794)
- code:  
- interpretation: 

#### Model-based Adversarial Meta-Reinforcement Learning 
- source: NeurIPS 2020 
- method: AdMRL
- environment:
- paper link: [https://arxiv.org/pdf/2006.08875v2.pdf](https://arxiv.org/pdf/2006.08875v2.pdf)
- code: [https://github.com/LinZichuan/AdMRL](https://github.com/LinZichuan/AdMRL)
- interpretation: 

### optimization-based meta-RL
#### [Model-Agnostic Meta-Learning for Fast Adaptation of Deep Networks]({{ site.url }}/2021/06/03/MAML.html)
- source: ICML 2017
- method: MAML-RL
- environment:
  - 2D navigation (rllab)
  - locomotion (rllab)
- paper link: [https://arxiv.org/pdf/1703.03400.pdf](https://arxiv.org/pdf/1703.03400.pdf)
- code: 
  - [https://github.com/cbfinn/maml_rl(tensorflow)](https://github.com/cbfinn/maml_rl) 
  - [https://github.com/tristandeleu/pytorch-maml-rl](https://github.com/tristandeleu/pytorch-maml-rl)
- interpretation: 

#### [On First-Order Meta-Learning Algorithms]({{ site.url }}/2021/06/04/Reptile.html)
- source:	arXiv:1803.02999 2018
- method: Reptile
- environment:
  - few-shot image classification
    - mini-ImageNet 
    - Omniglot
- paper link: [https://arxiv.org/pdf/1803.02999.pdf](https://arxiv.org/pdf/1803.02999.pdf)
- code: 
  - [https://github.com/openai/supervised-reptile](https://github.com/openai/supervised-reptile) 
- interpretation: 
  - https://openai.com/blog/reptile/
  - https://lilianweng.github.io/lil-log/2018/11/30/meta-learning.html#reptile

#### Meta-Reinforcement Learning of Structured Exploration Strategies
- source: NeurIPS 2018
- method: MAESN (model agnostic exploration with structured noise)
- environment:
  - robotic locomotion (rllab)
  - object manipulation
- paper link: [https://arxiv.org/pdf/1802.07245.pdf](https://arxiv.org/pdf/1802.07245.pdf)
- code: [https://github.com/russellmendonca/maesn_suite](https://github.com/russellmendonca/maesn_suite)
- interpretation: 
  - [https://zhuanlan.zhihu.com/p/63072582](https://zhuanlan.zhihu.com/p/63072582)

#### Some Considerations on Learning to Explore via Meta-Reinforcement Learning
- source: ICLR 2018 
- method: 
  - E-MAML(optimization-based)
  - E-$RL^2$(model-based)
- environment:
  - [Krazy World](https://github.com/bstadie/krazyworld)
- paper link: [https://arxiv.org/pdf/1803.01118v2.pdf](https://arxiv.org/pdf/1803.01118v2.pdf)
- code: 
  - [https://github.com/geyang/e-maml](https://github.com/geyang/e-maml) 
- interpretation: 

#### ProMP: Proximal Meta-Policy Search
- source: ICLR 2019
- method: ProMP 
- environment:
  - locomotion(gym & Mujoco)
    - HalfCheetahFwdBack
    - AntRandDir
    - HopperRandParams
    - WalkerFwdBack
    - HumanoidRandDir
    - WalkerRandParams
- paper link: [https://openreview.net/pdf?id=SkxXCi0qFX](https://openreview.net/pdf?id=SkxXCi0qFX)
- code: [https://github.com/jonasrothfuss/promp](https://github.com/jonasrothfuss/promp) 

#### Efficient Off-Policy Meta-Reinforcement Learning via Probabilistic Context Variables
- source: ICML2019
- method: PEARL (probabilistic embeddings for actor-critic RL)
- environment:
  - robotic locomotion (MuJoCo, MuJoCo200, MuJoCu133)
- paper link: [https://arxiv.org/pdf/1903.08254.pdf](https://arxiv.org/pdf/1903.08254.pdf)
- code: [https://github.com/katerakelly/oyster](https://github.com/katerakelly/oyster)
- interpretation: 
  - [https://bair.berkeley.edu/blog/2019/06/10/pearl/](https://bair.berkeley.edu/blog/2019/06/10/pearl/)

#### Learning to Adapt in Dynamic, Real-World Environments Through Meta-Reinforcement Learning
- source: ICLR 2019
- method: 
  - Model-Based Meta-Reinforcement Learning (train time)
  - Online Model Adaptation (test time)
- environment:
  - Mujoco
    - half cheetah:disabled joint, sloped terrain, pier 
    - Ant: crippled leg
  - real world robot
- paper link: [https://arxiv.org/pdf/1803.11347v6.pdf](https://arxiv.org/pdf/1803.11347v6.pdf)
- code:  
  - [https://github.com/iclavera/learning_to_adapt](https://github.com/iclavera/learning_to_adapt)
- interpretation: 
  - [https://sites.google.com/berkeley.edu/metaadaptivecontrol](https://sites.google.com/berkeley.edu/metaadaptivecontrol)

#### Meta-Q-Learning 
- source: ICLR 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/1910.00125.pdf](https://arxiv.org/pdf/1910.00125.pdf)
- code:  
- interpretation: 

#### [Decoupling Exploration and Exploitation for Meta-Reinforcement Learning without Sacrifices]({{ site.url }}/2021/06/05/dream.html)
- source:	ICML 2021
- method: Dream
- environment:
  - [gym-miniworld 3D navigation](https://github.com/maximecb/gym-miniworld)
- paper link: [https://arxiv.org/pdf/2008.02790v2.pdf](https://arxiv.org/pdf/2008.02790v2.pdf)
- code: 
  - [https://github.com/ezliu/dream](https://github.com/ezliu/dream)
- interpretation: 
  - [https://ezliu.github.io/dream/](https://ezliu.github.io/dream/)

#### Meta Learning via Learned Loss 
- source: ICPR 2021
- method: ML^3
- environment:
- paper link: [https://arxiv.org/pdf/1906.05374.pdf](https://arxiv.org/pdf/1906.05374.pdf) 
- code:  
- interpretation: 


### 未分类
#### Alchemy: A structured task distribution for meta-reinforcement learning
- source: arXiv:2102.02926 preprint 2021
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2102.02926v1.pdf](https://arxiv.org/pdf/2102.02926v1.pdf)
- code: 
  - [https://github.com/deepmind/dm_alchemy](https://github.com/deepmind/dm_alchemy)
- interpretation: 
  - [https://deepmind.com/research/publications/alchemy](https://deepmind.com/research/publications/alchemy)

#### Learning to Learn How to Learn: Self-Adaptive Visual Navigation Using Meta-Learning
- source: CVPR 2019
- method: savn 
- environment:
  - 3D navigation (ai2thor)
- paper link: [https://arxiv.org/pdf/1812.00971v2.pdf](https://arxiv.org/pdf/1812.00971v2.pdf)
- code:  
  - [https://github.com/allenai/savn](https://github.com/allenai/savn)
- interpretation: 

#### Learning Robust State Abstractions for Hidden-Parameter Block MDPs
- source: ICLR2021
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2007.07206v4.pdf](https://arxiv.org/pdf/2007.07206v4.pdf)
- code:  
- interpretation: 

#### Meta reinforcement learning as task inference
- source:	arXiv:1905.06424 2019
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/1905.06424v2.pdf](https://arxiv.org/pdf/1905.06424v2.pdf) 
- code:  
- interpretation: 

#### MELD: Meta-Reinforcement Learning from Images via Latent State Models 
- source: CoRL 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2010.13957v2.pdf](https://arxiv.org/pdf/2010.13957v2.pdf)
- code:  
  - [https://github.com/tonyzhaozh/meld](https://github.com/tonyzhaozh/meld)
- interpretation: 
  - [https://sites.google.com/view/meld-lsm](https://sites.google.com/view/meld-lsm)


#### Meta Reinforcement Learning with Task Embedding and Shared Policy 
- source: IJCAI 2019
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/1905.06527v3.pdf](https://arxiv.org/pdf/1905.06527v3.pdf)
- code: [https://github.com/llan-ml/tesp](https://github.com/llan-ml/tesp)
- interpretation: 

#### Fast Adaptive Task Offloading in Edge Computing based on Meta Reinforcement Learning 
- source: ITPDS 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2008.02033v5.pdf](https://arxiv.org/pdf/2008.02033v5.pdf)
- code: [https://github.com/linkpark/metarl-offloading](https://github.com/linkpark/metarl-offloading)
- interpretation: 


#### Learning Associative Inference Using Fast Weight Memory
- source: ICLR 2021
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2011.07831v2.pdf](https://arxiv.org/pdf/2011.07831v2.pdf)
- code: [https://github.com/ischlag/Fast-Weight-Memory-public](https://github.com/ischlag/Fast-Weight-Memory-public)
- interpretation: 

#### Few-Shot Complex Knowledge Base Question Answering via Meta Reinforcement Learning
- source: EMNLP 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2010.15877v1.pdf](https://arxiv.org/pdf/2010.15877v1.pdf)
- code: [https://github.com/DevinJake/MRL-CQA](https://github.com/DevinJake/MRL-CQA)
- interpretation: 


#### Meta Reinforcement Learning with Autonomous Inference of Subtask Dependencies 
- source: ICLR 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2001.00248v2.pdf](https://arxiv.org/pdf/2001.00248v2.pdf)
- code: [https://github.com/srsohn/msgi](https://github.com/srsohn/msgi)
- interpretation: 

#### Loaded DiCE: Trading off Bias and Variance in Any-Order Score Function Gradient Estimators for Reinforcement Learning
- source: NeurIPS 2019
- method: 
- environment:
- paper link: [http://papers.nips.cc/paper/9026-loaded-dice-trading-off-bias-and-variance-in-any-order-score-function-gradient-estimators-for-reinforcement-learning.pdf](http://papers.nips.cc/paper/9026-loaded-dice-trading-off-bias-and-variance-in-any-order-score-function-gradient-estimators-for-reinforcement-learning.pdf)
- code: [https://github.com/oxwhirl/loaded-dice](https://github.com/oxwhirl/loaded-dice)
- interpretation: 

#### Causal Reasoning from Meta-reinforcement Learning
- source: ICLR 2019
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/1901.08162v1.pdf](https://arxiv.org/pdf/1901.08162v1.pdf) 
- code: [https://github.com/kantneel/causal-metarl](https://github.com/kantneel/causal-metarl)
- interpretation: 

#### Introducing Neuromodulation in Deep Neural Networks to Learn Adaptive Behaviours 
- source:	arXiv:1812.09113 preprint 2019 
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/1812.09113v3.pdf](https://arxiv.org/pdf/1812.09113v3.pdf)
- code: [https://github.com/nvecoven/nmd_net](https://github.com/nvecoven/nmd_net)
- interpretation: 

#### Policy Gradient RL Algorithms as Directed Acyclic Graphs
- source: 	arXiv:2012.07763 preprint 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2012.07763v2.pdf](https://arxiv.org/pdf/2012.07763v2.pdf)
- code: [https://github.com/jjgarau/DAGPolicyGradient](https://github.com/jjgarau/DAGPolicyGradient)
- interpretation: 

#### Evolving Inborn Knowledge For Fast Adaptation in Dynamic POMDP Problems
- source: GECCO 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2004.12846v2.pdf](https://arxiv.org/pdf/2004.12846v2.pdf)
- code: [https://github.com/dlpbc/penn-a](https://github.com/dlpbc/penn-a)
- interpretation: 

#### Model-Based Meta-Reinforcement Learning for Flight with Suspended Payloads
- source: RA-L 2021 
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2004.11345v2.pdf](https://arxiv.org/pdf/2004.11345v2.pdf)
- code: [https://github.com/suneelbelkhale/model-based-meta-rl-for-flight](https://github.com/suneelbelkhale/model-based-meta-rl-for-flight)
- interpretation: 

#### Hierarchical Meta Reinforcement Learning for Multi-Task Environments
- source: ICLR 2021
- method: 
- environment:
- paper link: [https://openreview.net/pdf?id=u9ax42K7ND](https://openreview.net/pdf?id=u9ax42K7ND)
- code: [https://github.com/MeSH-ICLR/MEtaSoftHierarchy](https://github.com/MeSH-ICLR/MEtaSoftHierarchy)
- interpretation: 

#### Modeling and Optimization Trade-off in Meta-learning
- source: NeurIPS 2020
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2010.12916v2.pdf](https://arxiv.org/pdf/2010.12916v2.pdf)
- code: [https://github.com/intel-isl/MetaLearningTradeoffs](https://github.com/intel-isl/MetaLearningTradeoffs)
- interpretation: 

#### Meta-Learning of Structured Task Distributions in Humans and Machines 
- source: ICLR 2021
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2010.02317v3.pdf](https://arxiv.org/pdf/2010.02317v3.pdf)
- code: [https://github.com/sreejank/Compositional_MetaRL](https://github.com/sreejank/Compositional_MetaRL)
- interpretation: 

#### Offline Meta Learning of Exploration
- source:	arXiv:2008.02598 preprint 2021
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2008.02598v3.pdf](https://arxiv.org/pdf/2008.02598v3.pdf)
- code: [https://github.com/Rondorf/BOReL](https://github.com/Rondorf/BOReL)
- interpretation: 

#### Meta-Reinforcement Learning for Reliable Communication in THz/VLC Wireless VR Networks
- source: ICC 2021
- method: 
- environment:
- paper link: [https://arxiv.org/pdf/2102.12277v1.pdf](https://arxiv.org/pdf/2102.12277v1.pdf)
- code: [https://github.com/wyy0206/THzVR](https://github.com/wyy0206/THzVR)
- interpretation: 

<!--
#### 
- source: 
- method: 
- environment:
- paper link: 
- code:  
- interpretation: 

-->