---
layout: post
title: Snake Skin Rendering (CEIG 2023)
date: 2023-07-06 13:32:20 +0300
description: Multilayered appearance model based on the anatomy of the snake skin capable of reproducing the main appearance features on snake colors such as the highly specular iridescent colors and dark diffuse skin. The material was implemented as a BSDF layered material inside the popular physically-based renderer Mitsuba. # Add post description (optional)
img: snake_rendering.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Appearance Modeling, Rendering]
---

This project started as a bachelor thesis of a talented student (Diego Bielsa) that I supervised together with [Adolfo Muñoz](https://webdiis.unizar.es/~amunoz/es/) at the [Graphics and Imaging Lab](https://graphics.unizar.es/) and later it was presented at the Spanish Computer Graphics Conference ([CEIG 2023, Palma de Mallorca](https://www.eurographics.es/ceig23/)) under the title "A Biologically-Inspired Appearance Model for Snake Skin". The implementation consists of a multi-layered material implemented inside the physically-based renderer [Mitsuba 0.6](https://www.mitsuba-renderer.org/index_old.html) using the [Position-Free Monte Carlo](https://shuangz.com/projects/layered-sa18/) formulation. The top layer is a thin layer responsible for the specular iridescent reflection using a [practical iridescent microfacet model](https://belcour.github.io/blog/research/publication/2017/05/01/brdf-thin-film.html), while the bottom layer is a diffuse highly-absorbing layer designed to reproduce the dark diffuse appearance that highlight the iridescent colors of the snake skin. If you would like to know more about this project, then please visit the official project website [Snake Appearance Model](https://graphics.unizar.es/projects/SnakeSkinAppearance_2023/). Below you can see a beautiful rendering of a snake 3D model using our practical snake skin reflectance model roughly matching the general appearance of a Xenopeltis Unicolor!

![Rendering Xenopeltis Unicolor]({{site.baseurl}}/assets/img/xenopeltis_unicolor_render.png)

Team Members: Juan Raul Padron Griffe, [Diego Bielsa](https://github.com/DiegoBielsa)  

[Github repository](https://github.com/juanraul8/SnakeSkin)(Coming soon)

If you are interested in reptiles and their beautiful skin colours (pigmentary and structural) and skin colour patterns, then I would strongly encourage you to visit the official website of the [Laboratory of Artificial & Natural Evolution](https://www.lanevol.org/) at the University of Geneva!
