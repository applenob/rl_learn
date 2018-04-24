# 强化学习学习笔记

## 课程笔记

- [David Silver 的 Reinforcement Learning 课程学习笔记。](https://github.com/applenob/rl_learn/blob/master/class_note.ipynb)
- [课程对应的PPT](https://github.com/applenob/rl_learn/blob/master/slides)
- [Sutton 的 Reinforcement Learning: An Introduction书本学习笔记](https://github.com/applenob/rl_learn/blob/master/reinforcement_learning.ipynb)
- [书本的pdf](https://github.com/applenob/rl_learn/blob/master/book)
    - [2017-6](https://github.com/applenob/rl_learn/blob/master/book/bookdraft2017june19.pdf)
    - [second edition](https://github.com/applenob/rl_learn/blob/master/book/bookdraft2017june19.pdf)

## 实验目录

所有的实验源代码都在`lib`目录下，来自[dennybritz](https://github.com/dennybritz/reinforcement-learning)，这里只做解读和归总。

- [Gridworld](https://github.com/applenob/rl_learn/blob/master/1_gridworld.ipynb)：对应MDP的**Dynamic Programming**
- [Blackjack](https://github.com/applenob/rl_learn/blob/master/2_blackjack.ipynb)：对应Model Free的**Monte Carlo**的Planning和Controlling
- [Windy Gridworld](https://github.com/applenob/rl_learn/blob/master/3_windy_gridworld.ipynb)：对应Model Free的**Temporal Difference**的On-Policy Controlling，**SARSA**。
- [Cliff Walking](https://github.com/applenob/rl_learn/blob/master/4_cliff_walking.ipynb)：对应Model Free的Temporal Difference的Off-Policy Controlling，Q-learning。
- [Mountain Car](https://github.com/applenob/rl_learn/blob/master/5_mountain_car.ipynb)：对应Q表格很大无法处理（state空间连续）的Q-Learning with Linear Function Approximation。
- [Atari](https://github.com/applenob/rl_learn/blob/master/6_atari.ipynb)：对应Deep-Q Learning。
