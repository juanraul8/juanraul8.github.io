---
layout: post
title: Foundation Cosmetics Rendering (EGSR 2024)
date: 2024-07-01 8:00:00 +0300
description: Multilayered appearance model inspired by the specific characteristics of cosmetics foundation components capable of stacking multiple cosmetic products on top of a digital human skin. The material was implemented as a BSDF layered material inside the popular physically-based renderer PBRT. # Add post description (optional)
img: cosmetics_shinier_layer.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Appearance Modeling, Rendering]
---

We started this project two years ago lead by Dario Lanza when we visit [Jeppe Frisvad](https://people.compute.dtu.dk/jerf/) as part of our first secondment. The project was a collaboration between three research groups: [Graphics and Imaging Lab](https://graphics.unizar.es/), [DTU Visual Computing Section](https://www.compute.dtu.dk/sections/visual-computing) and [Media Design and Image Reproduction](https://liu.se/en/research/media-design-and-image-reproduction). Our work is going to be presented by Dario Lanza at the Eurographics Symposium on Rendering ([EGSR 2024, South Kensington, London](https://www.egsr2024.uk/)) under the title "Practical Appearance Model for Foundation Cosmetics". We represent each individual layer as a stochastic participating medium with two types of scatterers inspired by the microscopic constituents inside foundation cosmetics that mimic the most prominent visual features of these cosmetics: diffuse scatterers responsible for the matte appearance and specular platetets responsible for the glossy looks. The implementation consists of a multi-layered material implemented inside the physically-based renderer [PBRT version 4](https://github.com/mmp/pbrt-v4) using the [Position-Free Monte Carlo](https://shuangz.com/projects/layered-sa18/) formulation. The specular platelets are modelled using the [SGGX microflake](https://research.nvidia.com/publication/2015-08_sggx-microflake-distribution) phase function, while the diffuse particles are modelled with a two-lobe Henyey-Greenstein phase functions. If you would like to know more about this project, then please visit the official project website [Practical Appearance Model for Foundation Cosmetics](https://graphics.unizar.es/projects/CosmeticsAppearance_2024/). Below you can find a practical example where we add two cosmetics layers on top of a white female character's skin (left, bottom layer): a matte finish (center, middle layer) and a red shinier layer (right, top layer).   

![Rendering of foundation cosmetics]({{site.baseurl}}/assets/img/cosmetics_appearance_teaser.png)

Team Members: [Dario Lanza](https://dariolanza95.github.io/), Juan Raul Padron Griffe, [Alina Pranovich](https://orbit.dtu.dk/en/persons/alina-pranovich)  

[Github repository](https://github.com/dariolanza95/cosmetic_project) (Coming soon)

Carlos Aliaga and his colleagues recently release the source code of [BioSkin](https://github.com/facebookresearch/BioSkin). An interesting technique that can predict the biophysical skin properties from RGB reflectance and we think could potentially be combined with our appearance model in order to render the cosmetic foundations on different skin types.  