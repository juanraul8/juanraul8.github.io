---
layout: post
title: Neural Relighting
date: 2019-10-18 13:32:20 +0300
description: Extension of the Deferred Neural Rendering pipeline to perform relighting tasks. This is a new paradigm for image synthesis that combines the traditional graphics pipeline with learnable Neural Textures. # Add post description (optional)
img: neural_relighting.gif # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Neural Rendering, Relighting]
---
<p align="center">
  <img src="{{site.baseurl}}/assets/img/neural_relighting_architecture.png">
</p>

For my guided research project, we present an image-based relighting method that can synthesize scenes under novel lighting using image synthesis models based on deep learning. Our method extends [the Deffered Neural Rendering pipeline](https://justusthies.github.io/posts/deferred-neural-rendering/) to perform relighting tasks. This pipeline combines the traditional graphics pipeline with learnable components: neural textures and deferred neural ren- derer. We evaluate extensively the effectiveness of our approach in several experiments, on both synthetic and real scenes. Results prove that Neural Rendering pipeline is able to reproduce complex relighting tasks like modeling high frequency lighting effects such as specularities and shadows.

Results on [Light Stage Dataset](https://vgl.ict.usc.edu/Data/LightStage/)

![Helmet Front]({{site.baseurl}}/assets/img/helmet_front.gif)
![Fighting Knight]({{site.baseurl}}/assets/img/fighting_knight.gif)
![Plant]({{site.baseurl}}/assets/img/plant.gif)

Advisor: [Justus Thies](https://justusthies.github.io/)
Supervisor: [Matthias Niessner](https://niessnerlab.org/members/matthias_niessner/profile.html)

[Github repository](https://github.com/juanraul8/NeuralRelighting) [Document](https://drive.google.com/file/d/1el6d0RankNJh1N3E-JNAANRsfOPlohWt/view?usp=sharing)
