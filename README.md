# [WIP]强化学习的学习仓库

这是我个人学习**强化学习**的时候收集的比较经典的学习资料、笔记和代码，分享给所有人。

为了直接在GitHub上用markdown文件看公式，推荐安装chrome插件：[MathJax Plugin for Github](https://chrome.google.com/webstore/detail/mathjax-plugin-for-github/ioemnmodlmafdkllaclgeombjnmnbima)

## 入门指南

- [入门指南](learning_route.md)

## 课程笔记

- [David Silver 的 Reinforcement Learning 课程学习笔记。](class_note.ipynb)
- [课程对应的所有PPT](slides)
- Sutton 的 Reinforcement Learning: An Introduction书本学习笔记
  - [1. Introduction](notes/intro_note_01.md)
  - [2. Multi-armed Bandits](notes/intro_note_02.md)
  - [3. Finite Markov DecisionProcesses](#notes/intro_note_03.md)
  - [4. Dynamic Programming](notes/intro_note_04.md)
  - [5. Monte Carlo Methods](notes/intro_note_05.md)
  - [6. Temporal-Difference Learning](notes/intro_note_06.md)
  - [7. n-step Bootstrapping](notes/intro_note_07.md)
  - [8. Planning and Learning with Tabular Methods](notes/intro_note_08.md)
  - [9. On-policy Prediction with Approximation](notes/intro_note_09.md)
  - [10. On-policy Control with Approximation](notes/intro_note_10.md)
  - [11. Off-policy Methods with Approximation](notes/intro_note_11.md)
  - [12. Eligibility Traces](notes/intro_note_12.md)
  - [13. Policy Gradient Methods](notes/intro_note_13.md)
  - [14. Psychology](notes/intro_note_14.md)
  - [15. Neuroscience](notes/intro_note_15.md)
  - [16. Applications and Case Studies](notes/intro_note_16.md)
  - [17. Frontiers](notes/intro_note_17.md)

- [书本的各版本pdf](book)
  - [2017-6 draft](book/bookdraft2017june19.pdf)
  - [2018 second edition](book/bookdraft2018.pdf)

## 实验目录

所有的实验源代码都在`lib`目录下，来自[dennybritz](https://github.com/dennybritz/reinforcement-learning)。在原先代码的基础上，增加了对实验背景的具体介绍、代码和公式的对照。

- [Gridworld](exp/1_gridworld.ipynb)：对应**MDP**的**Dynamic Programming**
- [Blackjack](exp/2_blackjack.ipynb)：对应**Model Free**的**Monte Carlo**的Planning和Controlling
- [Windy Gridworld](exp/3_windy_gridworld.ipynb)：对应**Model Free**的**Temporal Difference**的**On-Policy Controlling**：**SARSA**。
- [Cliff Walking](exp/4_cliff_walking.ipynb)：对应**Model Free**的**Temporal Difference**的**Off-Policy Controlling**：**Q-learning**。
- [Mountain Car](exp/5_mountain_car.ipynb)：对应Q表格很大无法处理（state空间连续）的**Q-Learning with Linear Function Approximation**。
- [Atari](exp/6_atari.ipynb)：对应**Deep-Q Learning**。

## 其他重要学习资料：

- [WildML的博客](http://www.wildml.com/2016/10/learning-reinforcement-learning/)
- [David Silver’s Reinforcement Learning Course](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)
- [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html)
- [书本的python代码实现](https://github.com/ShangtongZhang/reinforcement-learning-an-introduction)
