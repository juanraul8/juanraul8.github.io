---
layout: post
title: Deep Reinforcement Learning for Protein Folding
date: 2018-10-2 13:32:20 +0300
description: AlphaGo algorithm implementation in C++ 17 for the protein folding problem. # Add post description (optional)
img: master_praktikum.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Protein Folding, Reinforcement Learning]
---

The protein structure determines properties and functions of the protein. Therefore, scientistic can develop drugs for this specific unique protein shape in order to cure diseases. Nowadays, Machine Learning methods arise as an alternative to the costly experimentation techniques (cryo-electron microscopy, nuclear magnetic resonance, X-ray crystallography) to help accelerate research.

For the [Hands-on Deep Learning for Computer Vision](https://www.in.tum.de/cg/teaching/winter-term-1718/3d-scanning-motion-capture/) practical course at the Technical University of Munich, we implement the infamous [AlphaGo](https://www.nature.com/articles/nature16961) algorithm in C++ to address the protein folding problem with the reinforcement learning approach. The main idea of the algorithm is training a neural network to estimate the policy and the values estimates, where the policy is improved by looking ahead into the future via Monte Carlo Tree Search guided by the value network. The environment (Rosetta 2017.39) and the Monte Carlo Tree Search algorithm were implemented in C++ 17, while the neural network was written in Python (TensorFlow 1.4.1). We rely on the TensorRT library to improve significantly the performance of the neural network inference. As a result, we could speed up the implementation 18.95 times regarding to the python version. Nevertheless, the approach is still unfeasible for large proteins (e.g. L = 332).

Results overfitting a single protein:

![Smooth Return]({{site.baseurl}}/assets/img/smooth_return.png)
![Value Loss]({{site.baseurl}}/assets/img/value_loss.png)
![Policy Loss]({{site.baseurl}}/assets/img/policy_loss.png)

Team Members: Matthias Humt, [Felix Opolka](https://felixopolka.me/)  
Instructors: [Vladimir Golkov](https://vision.in.tum.de/members/golkov), [Daniel Cremers](https://vision.in.tum.de/members/cremers)

[Presentation](https://drive.google.com/file/d/1MO6883uBrZXU8mwp9gbQin5ssAZYthNi/view?usp=sharing)

DeepMind implemented successfully this project idea in a system called [AlphaFold](https://deepmind.com/blog/article/AlphaFold-Using-AI-for-scientific-discovery). If you want to know more about cool projects in biomedicine, please contact Vladimir Golkov. Felix Opolka, which was the main author of this project, is currently working on cool publications about neural networks for graph-structured data.

