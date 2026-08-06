---
layout: post
title: Fabric Flyaways Rendering using Gaussian Primitives (SIGGRAPH Asia 2026)
date: 2026-07-28 12:00:00 +0300
description: A multi-scale Gaussian representation for rendering fabric flyaways, enabling efficient sheen and fuzziness effects with orders-of-magnitude lower storage  than curve- or volume-based approaches. Implemented as a custom integration and BSDF plugins in Mitsuba 3. 
img: fabric_flyaways.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Appearance Modeling, Rendering]
---

This project presents "Curvature-Aware Multi-Scale Gaussian Appearance Model for Fabric Flyaways," accepted to the conference track of SIGGRAPH Asia 2026. The work is co-authored by [Apoorv Khattar](https://research.manchester.ac.uk/en/persons/apoorv.khattar-postgrad) (University of Manchester), 
[Juan Raúl Padrón Griffe](https://juanraul8.github.io/) (Universidad de Zaragoza, I3A), [Ling-Qi Yan](https://sites.cs.ucsb.edu/~lingqi/) (Mohamed bin Zayed University of Artificial Intelligence), and [Zahra Montazeri](https://personalpages.manchester.ac.uk/staff/zahra.montazeri/) (University of Manchester). We introduce a multi-scale appearance model for fabric
flyaways — the fine, protruding fibers that give real-world textiles their characteristic fuzzy look and grazing-angle sheen — using 3D Gaussian primitives stored in a tileable texture instead of costly explicit curves or volumetric
representations. Individual fibers are compactly represented as anisotropic Gaussians and merged bottom-up into a mip-map-style pyramid as the pixel footprint grows, while a curvature-aware ray marching scheme updates the fabric's
silhouette at runtime without any precomputed curvature or normal maps. We evaluate our method against curve- and volume-based flyaway representations, achieving up to 7 to 40 times faster rendering while reducing storage requirements
by up to five orders of magnitude, all while providing greater artistic control over fiber density and protrusion depth. If you would like to know more about this project, please visit the official project website [Curvature-Aware
Multi-Scale Gaussian Appearance Model for Fabric Flyaways](https://graphics.unizar.es/projects/Khattar2026FabricFlyaways/). Below, we showcase the teaser with the main results.

![Fabric Flyaways Rendering (Teaser)]({{site.baseurl}}/assets/img/fabric_flyaways_teaser.png)

Team Members: [Apoorv Khattar](https://research.manchester.ac.uk/en/persons/apoorv.khattar-postgrad), Juan Raúl Padrón Griffe

The paper and supplemental material are available on the [project website](https://graphics.unizar.es/projects/Khattar2026FabricFlyaways/#downloads). Code and data will be released soon.

If you are interested in fabric appearance modeling and Gaussian-based rendering more broadly, then I would strongly encourage you to take a look at the following works: [3D Gaussian Splatting for Real-Time Radiance Field Rendering](https://dl.acm.org/doi/10.1145/3592433),
which introduced Gaussian primitives for real-time rendering and directly inspired our multi-scale Gaussian representation of flyaways, and [A Hierarchical 3D Gaussian Representation for Real-Time Rendering of Very Large Datasets](https://dl.acm.org/doi/10.1145/3658160),
whose bottom-up level-of-detail philosophy we adapt into our own mip-map-style merging scheme. For the appearance model driving our Gaussian flyaways, see [A Practical Ply-Based Appearance Model of Woven Fabrics](https://dl.acm.org/doi/10.1145/3414685.3417777),
whose BCSDF formulation we use to shade each Gaussian fiber. On the fabric side, [A Realistic Multi-Scale Surface-Based Cloth Appearance Model](https://dl.acm.org/doi/10.1145/3641519.3657426) models sheen analytically and serves as
our closest surface-based comparison point, while [A Texture-Free Practical Model for Realistic Surface-Based Rendering of Woven Fabrics](https://onlinelibrary.wiley.com/doi/10.1111/cgf.15283) provides the base fabric layer we build
our flyaways on top of in our real-photograph comparisons. For explicit curve-based fiber rendering, read [Matching Real Fabrics with Micro-Appearance Models](https://dl.acm.org/doi/10.1145/2818648), which we use as our reference
representation, and for the volumetric alternative, see [Building Volumetric Appearance Models of Fabric Using Micro-CT Imaging](https://dl.acm.org/doi/10.1145/2670517). For a broader introduction to fabric rendering as a whole, 
watch the SIGGRAPH Asia 2024 course [Recent Advances in Realistic Cloth Rendering](https://dl.acm.org/doi/10.1145/3680532.3689587) presented by [Junqiu Zhu](https://junqiuzhu.github.io/), [Zahra Montazeri](https://personalpages.manchester.ac.uk/staff/zahra.montazeri/), 
[Matt Jen-Yuan Chiang](https://mattchiangvfx.com/), and [Ling-Qi Yan](https://sites.cs.ucsb.edu/~lingqi/).