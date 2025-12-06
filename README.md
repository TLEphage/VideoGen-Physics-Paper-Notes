# VideoGen-Physics-Paper-Notes
基于物理遵循的视频生成相关论文及笔记

## 研究背景

现在大多数的视频生成工作都是数据驱动的，但是不太理解一些物理知识，比如连续运动，或者穿模，碰撞这一类的就做的不是很好
目前主要想解决非连续运动，不局限于单个物体，单个多个都能做
现有的数据集都是视觉上的，没有物理参数信息，我们希望数据集能控制物理参数，可以考虑做交互

## 调研阶段

- 调研数据集包括哪些运动（连续和非连续都包括），连续又包括哪些，比如自由落体，水平抛射、抛物线抛射、斜坡滑动、斜坡向上滑动这些场景
- 留意物理参数

- **VLIPP: Towards Physically Plausible Video Generation  with Vision and Language Informed Physical Prior**
  - [paper](https://arxiv.org/abs/2503.23368)
  - [project page](https://madaoer.github.io/projects/physically_plausible_video_generation/)
  - [repo](https://github.com/Madaoer/VLIPP)
- **PhysCtrl: Generative Physics for Controllable and Physics-Grounded Video Generation**
  - [paper](https://arxiv.org/abs/2509.20358)
  - project page
  - repo
- **NEWTONGEN: PHYSICS-CONSISTENT AND CONTROLLABLE TEXT-TO-VIDEO GENERATION VIA NEURAL  NEWTONIAN DYNAMICS**
  - [paper](https://arxiv.org/abs/2509.21309)
  - project page
  - repo
- **MORPHEUS: BENCHMARKING PHYSICAL REASONING OF VIDEO  GENERATIVE MODELS WITH REAL PHYSICAL EXPERIMENTS**
  - [paper](https://arxiv.org/abs/2504.02918)
  - project page
  - repo