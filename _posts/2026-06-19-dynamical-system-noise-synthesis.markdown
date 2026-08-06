---
layout: post
title: Dynamical System for Blue Noise (EGSR 2026)
date: 2026-06-19 12:00:00 +0300
description: A unified particle dynamics framework for spectral noise point distribution synthesis, transforming arbitrary input distributions into blue, pink, and red noise patterns within a single simulation pipeline. We showcase applications of the framework on image stippling, object placement, and Monte Carlo rendering. The framework is implemented in Python (NumPy, SciPy's cKDTree, and Numba) and results visualized via Blender's bpy API and evaluated in Monte Carlo rendering through PBRT v4.
img: dynamical_system_blue_noise.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Sampling, Noise Synthesis, Rendering, Simulation]
---

This project presents "A Dynamical System for Spectral Noise Synthesis," accepted to the symposium track of the Eurographics Symposium on Rendering ([EGSR 2026](https://egsr2026.inria.fr/)). The work is joint first-authored by
[Bojja Venu](https://www.dtu.dk/person/venu-bojja?id=172288) (Technical University of Denmark) and [Juan Raúl Padrón Griffe](https://juanraul8.github.io/) (Universidad de Zaragoza, I3A). We introduce a unified particle dynamics 
framework for spectral noise point distribution synthesis, capable of transforming arbitrary input distributions, such as an Archimedean spiral, into blue, pink, or red noise patterns within a single simulation pipeline. The framework
combines phasor vector field advection, which displaces particles along smooth spatially varying directions, with an inter-particle repulsion term that enforces local spatial uniformity, together forming a Langevin-type dynamical
system. An optional attraction term extends the same pipeline to pink and red noise through hierarchical spatial clustering, giving direct control over the spectral characteristics of the output distribution. We evaluate our method
against curl-noise jittering, Lloyd-based methods, and correlated multi-jittered sampling across several metrics, including anisotropy, discrepancy, spacing, coefficient of variation, and execution time, showing consistent improvements
in distribution quality at comparable computational cost. We showcase the framework across three graphics applications: color stippling, object placement, and Monte Carlo rendering. If you would like to know more about this project, 
please visit the official project website [A Dynamical System for Spectral Noise Synthesis](https://graphics.unizar.es/projects/Venu2026DynamicalNoiseSynthesis/). Below, we showcase example results and a schematic overview of the framework.

![Dynamical System for Noise Synthesis (Teaser)]({{site.baseurl}}/assets/img/dynamical_system_blue_noise_teaser.png)
![Mesh-Constrained Blue Noise on the Stanford Bunny]({{site.baseurl}}/assets/img/bunny_white_to_blue_comparison.png)

Team Members: [Bojja Venu](https://www.dtu.dk/person/venu-bojja?id=172288), Juan Raul Padron Griffe

The paper and supplemental material are available on the [project website](https://graphics.unizar.es/projects/Venu2026DynamicalNoiseSynthesis/#downloads). Code and data will be released soon.

If you are interested in spectral sampling and point distribution synthesis more broadly, then I would strongly encourage you to take a look at the following works: [Curl-Noise Jittering](https://github.com/jonasmb/curlnoisejittering), 
which generates blue noise by advecting points along a divergence-free vector field and serves as one of our baselines, and [Progressive Multi-Jittered Sample Sequences](https://onlinelibrary.wiley.com/doi/abs/10.1111/cgf.13472), 
whose PMJ02BN sampler we drive with our blue noise textures in our Monte Carlo rendering experiments. For screen-space error diffusion read [Screen-Space Blue-Noise Diffusion of Monte Carlo Sampling Error via Hierarchical Ordering of Pixels](https://dl.acm.org/doi/10.1145/3414685.3417881), 
which introduces the zsobol sampler we compare against. For physically-based simulation approaches read [Blue Noise Sampling Using an SPH-based Method](https://dl.acm.org/doi/10.1145/2816795.2818102), which generates blue noise by simulating
particle dynamics inspired by Smoothed Particle Hydrodynamics. The phasor-field formulation at the core of our advection step builds on [Procedural Phasor Noise](http://thibaulttricard.fr/project_page/phasor_noise/phasor.html)
by [Thibault Tricard](http://thibaulttricard.fr/). For extending blue noise generation to arbitrary spectra, see [Point Sampling with General Noise Spectrum](https://dl.acm.org/doi/10.1145/2185520.2185572). For a broader introduction
to sampling theory and its role in rendering, watch the SIGGRAPH course [My Favorite Samples](https://www.youtube.com/watch?v=bHDfETTS550), which includes PMJ sequences and blue-noise dithering.