# MsPacman-V5 Reinforcement Learning Project

## Overview

This project explores the application of three Reinforcement Learning (RL) algorithms—Deep Q-Network (DQN), Deep Deterministic Policy Gradient (DDPG), and Soft Actor-Critic (SAC)—to solve the MsPacman-V5 Atari environment. The primary objective is to compare the performance and stability of these algorithms in tackling this classic game.

## Algorithms Implemented

1. **Deep Q-Learning (DQN)**:
   - Combines Q-Learning with deep neural networks to approximate the Q-function.
   - Uses experience replay and target networks for stable training.

2. **Deep Deterministic Policy Gradient (DDPG)**:
   - An actor-critic algorithm suitable for continuous action spaces.
   - Utilizes separate actor and critic networks, combined with experience replay and target networks.

3. **Soft Actor-Critic (SAC)**:
   - Optimized for continuous action spaces.
   - Implements maximum entropy to promote exploration and uses dual Q-networks for stability.

## Problem

The environment, MsPacman-V5, has a continuous observation space but discrete action space. We implemented custom reward functions to deal with the sparse reward structure of the game and improved agent learning by rewarding exploration and penalizing inaction.

## Key Features

- **Replay Buffer**: Efficient experience sampling for more stable learning.
- **Custom Reward System**: Additional rewards for exploration and penalties for inaction.
- **Convolutional Neural Networks**: Employed in all algorithms to process the game’s visual input.
- **Training Stability Techniques**: Polyak averaging and target networks are used to stabilize learning.

## Results

- **DQN**: Achieved the most stable learning curve, reaching a maximum reward of 1670.
- **DDPG**: Showed instability but had the potential to achieve higher rewards.
- **SAC**: Performance was hampered by the discrete action space, requiring more fine-tuning for convergence.

## Dependencies

- Python 3.x
- PyTorch
- OpenAI Gym
- Atari-Py
