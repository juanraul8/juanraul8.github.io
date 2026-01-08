---
layout: post
title: Procedural Multiscale Geometry (PG 2025)
date: 2025-10-17 13:32:20 +0300
description: A procedural framework for modeling multiscale volumetric materials using implicit surfaces and sphere tracing. It supports rich micro- and mesostructures, including microstructure reconstruction from image and distance values. The framework is implemented as procedural shaders in the NVIDIA OptiX ray tracing API. This project received a Best Paper (Honorable Mention) award. # Add post description (optional)
img: multiscale_bunny_rendering.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Geometry Modeling, Procedural Modeling, Appearance Modeling, Rendering]
---

This project is part of the doctoral thesis of [Bojja Venu](https://www.linkedin.com/in/bojja-venu-97a38b89/) and presents a framework inspired by hypertexture methods that synthesizes multiscale structures on the fly using implicit surfaces and sphere tracing, without precomputation. Venu presented the paper at the Pacific Graphics Conference ([Pacific Graphics 2025, Taipei](https://pg2025.nccu.edu.tw/)) under the title "Procedural Multiscale Geometry Modeling using Implicit Surfaces". The framework enables the creation of complex, multiscale spatially varying geometries like particles, fibers, pores, and layers using random but controlled space-filling implicit primitive distributions, and then apply spatially varying transformations. Additional operations support anisotropy, correlation, piling, and agglomeration effects. As a proof of concept, we show that the generated microstructures can be reconstructed from image and distance values defined by implicit surfaces using both first-order and gradient-free optimization methods. This reconstruction work was carried out as part of the master’s thesis of [Adam Bosek](https://www.linkedin.com/in/adambosak/) at the Technical University of Denmark, supervised by [Jeppe Frisvad](https://www.imm.dtu.dk/~jerf/), [Bojja Venu](https://www.linkedin.com/in/bojja-venu-97a38b89/), and myself. The implementation includes a Monte Carlo path tracer and procedural shaders developed using the NVIDIA OptiX 7.4 ray tracing API. If you would like to know more about this project, then please visit the official project website [Procedural Multiscale Geometry](https://graphics.unizar.es/projects/MultiscaleGeometry_2025/). Below, we showcase example results and a schematic overview of the framework’s features.

![Multiscale Geometry Framework (Results)]({{site.baseurl}}/assets/img/multiscale_geometry_teaser.png)
![Multiscale Geometry Framework (Overview)]({{site.baseurl}}/assets/img/multiscale_geometry_overview.png)

Team Members: [Bojja Venu](https://www.linkedin.com/in/bojja-venu-97a38b89/), [Adam Bosek](https://www.linkedin.com/in/adambosak/), Juan Raul Padron Griffe

We will share the GitHub repository of the modeling and reconstruction soon.  

It was truly an honor to have our work recognized by the computer graphics community, and we hope it inspires future research in the modeling, rendering, and simulation of multiscale materials.  

![Pacific Graphics Best Paper (Honorable Mention)]({{site.baseurl}}/assets/img/multiscale_geometry_best_paper.jpg)
