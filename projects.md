---
layout: default
title: Research Projects
---

# Research Projects

[← Back to Home](/)

---

## Granular & Deformable Object Manipulation

### DDBot: Differentiable Physics-Based Digging Robot for Unknown Granular Materials

*IEEE Transactions on Robotics, 2025 · vol. 42, pp. 152–169*

**Yang, X.**, Wei M., Ji Z., Lai Y.-K.

Manipulating granular materials such as sand and soil with precision is extremely difficult — their physical properties are unknown in advance and they behave in complex, unpredictable ways. DDBot addresses this by combining a GPU-accelerated differentiable physics simulator tailored for granular materials with gradient-based optimisation. The robot first identifies unknown material properties (system identification) and then optimises its digging strategy — all without prior knowledge of the material — achieving high-precision results when deployed directly in the real world (zero-shot transfer).

**Key contributions:**
- First framework to apply first-order gradient-based optimisation to differentiable granular material simulation
- Efficient convergence (5–20 min) for both system identification and skill optimisation
- Demonstrated high-precision zero-shot real-world deployment on sand and soil
- GPU-accelerated parallel simulation with automatic differentiation

<a href="https://arxiv.org/abs/2510.17335">📄 Preprint</a> &nbsp;·&nbsp;
<a href="https://doi.org/10.1109/TRO.2025.3636815">📰 Published Paper</a> &nbsp;·&nbsp;
<a href="https://www.youtube.com/watch?v=eoNx5V688H0">▶ Video Demo</a>

---

### Differentiable Physics-Based System Identification for Robotic Manipulation of Elastoplastic Materials

*International Journal of Robotics Research (IJRR), 2025*

**Yang, X.**, Ji Z., Lai Y.-K.

Materials like clay and dough deform permanently when manipulated — making them notoriously hard to simulate or control. This work introduces DPSI (Differentiable Physics-based System Identification), a framework that lets a robot arm estimate the physical properties of such materials (Young's modulus, Poisson's ratio, yield stress, friction) from just a single real-world interaction and incomplete 3D point clouds. The estimated parameters are physically interpretable — unlike neural network "black-box" approaches — and enable accurate simulation of long-horizon deformation behaviours.

**Key contributions:**
- Estimates material physics parameters from a single real-world robot interaction
- Works with incomplete, occluded 3D point cloud data from standard optical cameras
- Fully interpretable parameters (Young's modulus, Poisson's ratio, yield stress, friction)
- Simulation-to-real alignment enables high-precision long-horizon manipulation planning
- Fully open-sourced

<a href="https://arxiv.org/abs/2411.00554">📄 Preprint</a> &nbsp;·&nbsp;
<a href="https://doi.org/10.1177/02783649251334661">📰 Published Paper</a> &nbsp;·&nbsp;
<a href="https://www.youtube.com/watch?v=2-9JWRsQhTU">▶ Video Demo</a> &nbsp;·&nbsp;
<a href="https://ianyangchina.github.io/SI4RP-data/">🌐 Project Page & Code</a>

---

### AutomaChef: A Physics-Informed Demonstration-Guided Learning Framework for Granular Material Manipulation

*IEEE Transactions on Neural Networks and Learning Systems (TNNLS), 2025*

Wei M., **Yang X.**, Lai Y.-K., Tafrishi S.A., Ji Z.

Standard robot learning methods struggle with granular materials (e.g., grains, powder) because collecting training data is expensive and their physical properties are complex. AutomaChef bypasses costly data collection by using a differentiable physics-based simulator to automatically generate expert demonstrations via gradient-based optimisation, which then guide policy learning. The resulting policies successfully transfer to real-world granular transport tasks.

**Key contributions:**
- Differentiable granular material simulator built with the Taichi programming language
- Demonstrations generated automatically via gradient optimisation (no costly real-world data collection)
- Surpasses standard reinforcement learning, imitation learning, and prior task-specific methods
- Successfully deployed on real-world granular transport tasks

<a href="https://arxiv.org/abs/2406.09178">📄 Preprint</a> &nbsp;·&nbsp;
<a href="https://doi.org/10.1109/TNNLS.2025.3622482">📰 Published Paper</a>

---

### Celebi's Choice: Causality-Guided Skill Optimisation for Granular Manipulation via Differentiable Simulation

*IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2025*

Wei M., **Yang X.**, Yan J., Lai Y.-K., Ji Z.

Optimising robot skills for granular material manipulation (e.g., soil excavation and levelling) using differentiable simulation suffers from instability due to the highly nonlinear dynamics involved. Celebi addresses this by incorporating causal inference into the optimisation loop: it models causal relationships between task-relevant features (extracted from point cloud observations) and skill parameters, and uses these to adaptively adjust gradient update step sizes — improving both stability and convergence efficiency.

**Key contributions:**
- Causality-enhanced gradient-based optimisation for granular skill learning
- Differentiable simulation environment for granular material interactions
- Differentiable skill-to-action mapping enabling trajectory optimisation
- Adaptive step-size adjustment via causal inference improves stability and convergence

<a href="https://doi.org/10.1109/IROS60139.2025.11247432">📰 Published Paper</a>

---

## Affordance & Reinforcement Learning for Rigid Object Manipulation

### GAM: General Affordance-Based Manipulation for Contact-Rich Object Disentangling Tasks

*Neurocomputing, 2024 · vol. 578, 127386*

**Yang, X.**, Wu J., Lai Y.-K., Ji Z.

Disentangling objects that are in contact with each other — such as separating tangled cables or nested containers — requires a robot to understand fine-grained spatial affordances (where and how to grasp) and execute contact-rich motions. GAM proposes a general affordance-based manipulation framework that learns to predict these affordances and execute disentangling strategies for diverse object configurations.

**Key contributions:**
- General affordance prediction for contact-rich manipulation without task-specific engineering
- Handles diverse and unseen disentangling object configurations
- Combines affordance learning with goal-conditioned reinforcement learning
- Validated across multiple real and simulated contact-rich scenarios

<a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4606046">📄 Preprint</a> &nbsp;·&nbsp;
<a href="https://www.youtube.com/watch?v=Rao_Ctfh9BI">▶ Video Demo</a>

---

### Abstract Demonstrations and Adaptive Exploration for Efficient and Stable Multi-Step Sparse Reward Reinforcement Learning

*27th International Conference on Automation and Computing (ICAC), 2022*

**Yang, X.**, Ji Z., Wu J., Lai Y.-K.

Long-horizon robotic manipulation tasks with sparse rewards (e.g., stacking several blocks where only final success is rewarded) are extremely hard for standard deep RL. This paper proposes A²E, a technique that combines two human-inspired ideas: decomposing complex tasks into ordered sub-tasks and providing abstract demonstrations of the correct sub-task sequence, while training the agent to explore more freely on poorly learnt sub-tasks and more deterministically on well-mastered ones.

**Key contributions:**
- Decomposes complex multi-step tasks into ordered sub-task sequences with abstract demonstrations
- Adaptive exploration: more deterministic on mastered sub-tasks, more stochastic on poorly learnt ones
- Validated on grid-world and real robotic manipulation benchmarks
- Improves both learning efficiency and training stability over standard DRL baselines

---

### Efficient Hierarchical Reinforcement Learning for Mapless Navigation with Predictive Neighbouring Space Scoring

*IEEE Transactions on Automation Science and Engineering (TASE), 2023 · vol. 21, no. 4, pp. 5457–5472 · 21 citations*

Gao Y., Wu J., **Yang X.**, Ji Z.

Mapless robot navigation from raw high-dimensional sensor data (LiDAR, cameras) is expensive to learn end-to-end. This work proposes an efficient hierarchical RL framework using a novel sub-goal scoring model — Predictive Neighbouring Space Scoring (PNSS) — which estimates how explorable nearby positions are from the current observation. PNSS generates compact, meaningful sub-goals that guide a low-level navigation policy, dramatically reducing learning complexity.

**Key contributions:**
- Predictive Neighbouring Space Scoring (PNSS) model for compact sub-goal generation
- Hierarchical RL framework separating high-level goal selection from low-level navigation
- Reduces dimension and learning complexity versus end-to-end approaches from raw sensors
- Validated on challenging mapless navigation benchmarks

<a href="https://doi.org/10.1109/TASE.2023.3260307">📰 Published Paper</a>

---

### Recent Advances of Deep Robotic Affordance Learning: A Reinforcement Learning Perspective

*IEEE Transactions on Cognitive and Developmental Systems (TCDS), 2023 · vol. 15, no. 3, pp. 1139–1149*

**Yang, X.**, Ji Z., Wu J., Lai Y.-K.

A survey and analysis of deep robotic affordance learning — the study of how robots learn *where* and *how* to act on objects. This review classifies methods from a reinforcement learning perspective, discusses technical details and limitations, and proposes a promising future direction: RL-based affordance definitions that predict the consequences of arbitrary actions.

**Key contributions:**
- Comprehensive taxonomy of deep robotic affordance learning from an RL perspective
- Connects affordance theory (from psychology) with modern deep RL methods
- Identifies open challenges in observation, action spaces, representation, and real-world deployment
- Proposes action-consequence prediction as a unifying future direction

<a href="https://arxiv.org/abs/2303.05344">📄 Preprint</a> &nbsp;·&nbsp;
<a href="https://doi.org/10.1109/TCDS.2023.3277288">📰 Published Paper</a>

---

### Hierarchical Reinforcement Learning with Universal Policies for Multi-Step Robotic Manipulation

*IEEE Transactions on Neural Networks and Learning Systems (TNNLS), 2021 · vol. 33, no. 9, pp. 4727–4741 · **133 citations***

**Yang, X.**, Ji Z., Wu J., Lai Y.-K., Wei C., Liu G., Setchi R.

Teaching robots to perform long, multi-step manipulation tasks (e.g., pick, stack, insert in sequence) with sparse rewards is a fundamental challenge. This work proposes the Universal Option Framework (UOF), a hierarchical RL architecture where a high-level policy decomposes complex tasks into sub-goals and low-level universal policies are reused across sub-tasks, enabling efficient learning of long-horizon manipulation.

**Key contributions:**
- Hierarchical architecture decomposes long-horizon tasks into reusable sub-goals
- Universal low-level policies generalise across diverse sub-task instances
- Achieves efficient learning under sparse reward signals
- Demonstrated on challenging multi-step robotic manipulation benchmarks

<a href="https://ieeexplore.ieee.org/document/9366328">📰 Published Paper</a> &nbsp;·&nbsp;
<a href="https://www.youtube.com/watch?v=n_wQuf4r0qk">▶ Video Demo</a> &nbsp;·&nbsp;
<a href="https://github.com/IanYangChina/UOF-paper-code">💻 GitHub</a>

---

### An Open-Source Multi-Goal Reinforcement Learning Environment for Robotic Manipulation with PyBullet

*Towards Autonomous Robotic Systems (TAROS), 2021*

**Yang, X.**, Ji Z., Wu J., Lai Y.-K.

A re-implementation of OpenAI Gym's robotic manipulation benchmarks on the free, open-source PyBullet physics engine (replacing the commercial MuJoCo engine). Includes new APIs for joint control, image observations, and a built-in on-hand camera, plus a suite of novel multi-step, long-horizon, sparse-reward tasks designed to challenge goal-conditioned RL algorithms.

**Key contributions:**
- Full open-source re-implementation of multi-goal robotic manipulation benchmarks (no commercial license needed)
- New APIs: joint-space control, image observations, customisable & on-hand cameras
- Novel multi-step, long-horizon, sparse-reward task suite
- Validated parity with original MuJoCo environments using HER-DDPG

<a href="https://arxiv.org/abs/2105.05985">📄 Preprint</a> &nbsp;·&nbsp;
<a href="https://github.com/IanYangChina/pybullet_multigoal_gym">💻 GitHub</a>

---

*For a full publication list, visit my [Google Scholar profile](https://scholar.google.com/citations?user=pJoieqMAAAAJ). Last updated: March 2026.*
