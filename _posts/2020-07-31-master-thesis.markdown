---
layout: post
title: Face Relighting In The Wild
date: 2020-07-31 13:32:20 +0300
description: Given an arbitrary portrait image and a target lighting as inputs, the algorithm generates the relight version of the portrait image under the target lighting conditions. # Add post description (optional)
img: face_relighting.gif # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Neural Rendering, Relighting]
---
Relighting plays an essential role in realistically transferring objects from a captured environment into another one. In particular, current applications like telepresence need to relit faces
consistently with the illumination conditions of the target environment to offer an authentic
immersive experience. Traditional physically-based methods for portrait relighting rely on an
intrinsic image decomposition step, which requires to solve a challenging inverse rendering
problem in order to obtain the underlying face geometry, reflectance material and lighting.
Inaccurate estimation of these components usually leads to strong artifacts (e.g. artificial
highlights or ghost effects) in the subsequent relighting step. In recent years, several deep
learning architectures have been proposed to address this limitation. However, none of them
are free from these artifacts.

In my Master thesis, we propose a general framework for automatic relighting enhancement using
the [StyleGAN generator](https://github.com/NVlabs/stylegan) as a photorealistic portrait prior. Specifically, we apply the ratio
image-based face relighting to an artificial portrait dataset generated using the StyleGAN
model. Next, we refine this dataset by projecting back the relit samples into the StyleGAN
space. Then, we train an autoencoder network to relit portrait images from a source portrait
image and a target spherical harmonic lighting. We evaluate the proposed method on our
synthetic dataset, [the Laval face and lighting dataset](http://faces.hdrdb.com/) and [the Multi-PIE dataset](http://www.cs.cmu.edu/afs/cs/project/PIE/MultiPie/Multi-Pie/Home.html) both qualitatively and quantitatively. Our experiments prove that this method can enhance the state of
the art [single portrait relighting algorithm](https://zhhoper.github.io/dpr.html) for synthetic datasets. Unlike this algorithm, we
achieve these results relying on a synthetic dataset five times smaller employing a traditional
training scheme.

Results:  

![Obama Lights]({{site.baseurl}}/assets/img/obama_lights.gif)
![Obama Relighting]({{site.baseurl}}/assets/img/obama_relits.gif)

Advisor: [Justus Thies](https://justusthies.github.io/)
Supervisor: [Matthias Niessner](https://niessnerlab.org/members/matthias_niessner/profile.html)

[Github repository](https://github.com/juanraul8/face_relighting) [Document](https://drive.google.com/file/d/1soVfVDUHOFGJDmkesVl6FWo6E3jcTEnZ/view?usp=sharing)
