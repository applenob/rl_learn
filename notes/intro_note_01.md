# 1. Introduction

## 书本介绍

![book_cover](https://img1.doubanio.com/view/subject/l/public/s29867258.jpg)

[Reinforcement Learning](https://book.douban.com/subject/30323890/)

作者: Richard S. Sutton / Andrew G. Barto 

几乎是最权威的强化学习教材。

## 重要的符号表示

- $q_∗(a)$：动作a对应的真实价值（价值期望），true value (expected reward) of action a
- $Q_t(a)$：动作a在t时刻的估计价值，estimate at time t of $q_∗(a)$
- $N_t(a)$：在t时刻之前，动作a已经被选择的次数，number of times action a has been selected up prior to time t
- $H_t(a)$：在t时刻选择动作a的偏好程度，learned preference for selecting action a at time t
- $π_t(a)$：在t时刻选择动作a的概率，probability of selecting action a at time t
- $R_t$：给定策略$π_t$，在t时刻的期望奖励，estimate at time t of the expected reward given$π_t$

## 什么是强化学习

强化学习是“学习该如何去做”（learning what to do），即学习如何从**某个状态映射到某个行为，来最大化某个数值的奖励信号**。

## 强化学习的特征

强化学习两个最重要的特征：

- **试错**（trial-and-error search ）：agent需要不断尝试，通过reward的反馈学习策略。
- **延迟奖励**（delayed reward） ：某个时刻的action可能会对后面时刻的reward有影响（深远影响）。

### Exploit vs Explore

- **exploit**: 代表利用已有的信息去获得最大的奖励。
- **explore** 代表去探索一些没有尝试过的行为，去获得可能的更大的奖励。

## 强化学习的几个要素

- **policy**: 状态到行为的映射，定义agent在某个状态下应该如何采取行为，state $\rightarrow$ action。
- **reward function**: 在某个状态下，agent能够收到的**即时反馈**。
- **value function**: 衡量在某个状态下，能够获得的**长期反馈**。
- **modle (of the environment，可选的)**: 模型用来模拟环境的行为，**给定一个状态和动作，模型可以预测下一个状态和奖励**。

## RL vs Evolutionary Methods

- **Evolutionary Methods**（遗传算法，具体可以回顾[之前的博客](https://applenob.github.io/ga.html)），直接在policy空间中搜索，并计算最后的得分。通过一代代的进化来找寻最优policy。
- 遗传算法忽略了policy实际上是state到action的映射，它不关注agent和环境的互动，只看最终结果。

## 局限性

强化学习非常依赖**状态**（state）的概念。state既是策略函数和价值函数的输入，又是**环境模型**（model）的输入和输出。

## Tic-Tac-Toe（井字棋）

- ![tic-tac-toe](../res/ttt.png)
- 一个简单的应用强化学习的例子。
- 定义policy：任何一种局面下，该如何落子。
- 遗传算法解法：试很多种policy，找到最终胜利的几种，然后结合，更新。
- 强化学习解法：
  - 1.建立一张表格，state_num × 1，代表每个state下，获胜的概率，这个表格就是所谓的**value function**，即状态到价值的映射。
  - 2.跟对手下很多局。每次落子的时候，依据是在某个state下，选择所有可能的后继state中，获胜概率最大的（value最大的）。这种方法即贪婪法（Exploit）。偶尔我们也随机选择一些其他的state（Explore）。
  - 3.“back up”后继state的v到当前state上。$V(s)\leftarrow V(s)+\alpha[V(s')-V(s)]$，这就是所谓的**差分学习**（temporal-difference learning），这么叫是因为$V(s')-V(s)$是两个时间点上的两次估计的差。
