---
layout: post
title: Fractal Terrain Generation using Noise Synthesis
date: 2015-05-24 13:32:20 +0300
description: Intuitive tool using OpenGL to explore and evaluate several fractal algorithms and their associated parameters. # Add post description (optional)
img: bachelor_thesis.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Procedural Modeling, Terrain Generation, Fractals, Noise Synthesis]
---
In the last decades, the advances in modelling virtual worlds have been impressive and notorious, from primitive results (Alien, 1979) to visually complex ones (CryEngine, 2009). However, the process is mostly manual, laborious, repetitive and costly especially for large scenes. For this reason, an alternative approach called procedural modelling, where the content is created via a procedure or program, is becoming more popular. An open research challenge is the automatic generation of terrains, especially if we consider the inmense variety of shapes and appearances.

For my Bachelor thesis, we develop a terrain generator based on an extension of the noise synthesis technique that includes transformations in order to improve significantly the capacity and power of the heightmap generation. The fractal generator is able to synthesize several types of terrains such as a glacier, mountain range or plateau in an efficient and extensive way by using different base functions (value noise, [Perlin noise](https://mrl.nyu.edu/~perlin/paper445.pdf)) and transformations (domain distortion and filters). Furthermore, we implement a realtime 3D Viewer using OpenGL shaders in order to explore the generated heightmaps, which include features like triplanar texture mapping, detail maps, sky domes, Phong illumination model and a navigation map. Finally, we carried out several experiments in order to study and evaluate the impact of the different algorithms, base functions and transformations. 

Results:  

![Terrain Scene 1]({{site.baseurl}}/assets/img/terrain_1.png)
![Terrain Scene 2]({{site.baseurl}}/assets/img/terrain_2.png)
![Terrain Scene 3]({{site.baseurl}}/assets/img/terrain_3.png)

Advisor: [Hector Navarro](https://vision.in.tum.de/members/golkov)
Supervisor: [Rhadamés Carmona](https://www.linkedin.com/in/rhadam%C3%A9s-carmona-31b0081/)

This work was heavily inspired in three sources:  
[Real-time editing, synthesis, and rendering of infinite landscapes on GPUs](https://www.in.tum.de/cg/research/publications/2006/real-time-editing-synthesis-and-rendering-of-infinite-landscapes-on-gpus/)  
[Interactive GPU-based procedural heightfield brushes](https://graphics.tudelft.nl/Publications-new/2009/DB09a/)  
[Value Noise Derivatives](https://www.iquilezles.org/www/articles/morenoise/morenoise.htm)

[Document](https://drive.google.com/file/d/16PgIkpOOTXBhO0gBzbdN9-xLRofakXoz/view?usp=sharing) [Presentation](https://drive.google.com/file/d/1zJ1c0cwMw72YhUqXSgXJYB_Yn8ndSWZ3/view?usp=sharing)
