---
layout: post
title: Game Capture
date: 2018-09-28 13:32:20 +0300
description: C++ library for the extraction of ground truth labels and the internal game states of video games to train computer vision models for autonomous driving applications. # Add post description (optional)
img: game_capture.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Video Games, Data Capture]
---

The main goal of the Hiwi project at the chair of [Remote Sensing Technology](https://www.bgu.tum.de/lmf/startseite/) at the Technical University of Munich is collecting potentially useful information from video games in order to train computer vision models for autonomous driving applications. The project is inspired in the seminal publication [Playing for Data](https://download.visinf.tu-darmstadt.de/data/from_games/), where the authors show that acquired data from video games supplemented with real-world images significantly increases the accuracy of deep learning models for the semantic segmentation task. In addition, the acquisition pipeline reduces the amount of hand-labeled real-world data. We develop a prototype in C++ to collect in realtime the DirectX Frame Buffers (RGB, Stencils, Albedo, Irradiance, Specular, Normal) from the video game Grand Theft Auto V. Finally, we could also extract further internal game states (e.g. time of day, location, vehicle speed, etc) using the Script Hook V mod.  

In the second phase, we tried to capture data from other games based on the [Free Supervision from Video Games](http://www.philkr.net/fsv/) paper. The GameHook library wraps DirectX 11 to intercept and modify the rendering code of a particular game, including the injection of code into the vertex or pixel shaders. Unfortunately, the library failed to hook games like Project Cars 2 or Sebastian Loeb Rally.  

Results:

![Disparity Map]({{site.baseurl}}/assets/img/disparity_map.png)
![Normal Map]({{site.baseurl}}/assets/img/normal_map.png) 
![Instance Segmentation]({{site.baseurl}}/assets/img/object_id_map.png)

![Albedo Map]({{site.baseurl}}/assets/img/diffuse_map.png)
![Specular Map]({{site.baseurl}}/assets/img/specular_map.png)
![Irradiance Map]({{site.baseurl}}/assets/img/irradiance_map.png)

 
Advisors: [Sandra Aigner](https://www.bgu.tum.de/aigner/), [Lukas Liebel](https://www.bgu.tum.de/liebel/)  
Supervisor: [Marco Körner](https://www.bgu.tum.de/lmf/koerner/)

If you want to know more about the project, please contact Lukas Liebel and Sandra Aigner. They are really nice advisors and they are working in interesting projects. I would also suggest you to read this amazing post [GTA V - Graphics Study](http://www.adriancourreges.com/blog/2015/11/02/gta-v-graphics-study/) and play with the amazing RenderDoc tool.