---
layout: page
permalink: /building-facade-normal-estimation-crv/
title: "Building Facades to Normal Maps: Adversarial Learning from Single View Images"
description: Project page for our [`Building Facades to Normal Maps – Adversarial Learning from Single View Images`](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=kWAlOAkAAAAJ&citation_for_view=kWAlOAkAAAAJ:qjMakFHDy7sC) work accepted at [`CRV 2021`](https://www.computerrobotvision.org/).
nav: false
---

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-0" src="{{ site.baseurl }}/assets/img/CRV/teaser.png">
    </div>
</div>

---

<!-- Project page for our `Building Facades to Normal Maps– Adversarial Learning from Single View Images` work accepted at [`CRV 2021`](https://www.computerrobotvision.org/). -->

<!-- **Authors:** Mukul Khanna <sup>*</sup>, Tanu Sharma <sup>*</sup>, Ayyappa Swamy Thatavarthy, K. Madhava Krishna -->
**Authors:** Mukul Khanna\*, Tanu Sharma\*, Ayyappa Swamy Thatavarthy, K. Madhava Krishna

---

##### Abstract

Surface normal estimation is an essential component of several computer and robot vision pipelines. While this problem has been extensively studied, most approaches are geared towards indoor scenes and often rely on multiple modalities (depth, multiple views) for accurate estimation of normal maps.
Outdoor scenes pose a greater challenge as they exhibit significant lighting variation, often contain occluders, and structures like building facades are often ridden with numerous windows and protrusions.
Conventional supervised learning schemes excel in indoor scenes, but do not exhibit competitive performance when trained and deployed in outdoor environments. Furthermore, they are not geared towards real-time inference.
To tackle these challenges, we present an adversarial learning scheme that regularizes the output normal maps from a neural network to appear more realistic, by using a small number of precisely annotated examples.
Our method presents a lightweight and simpler architecture, while improving performance by at least 2x to 4x across most metrics.

---

#### Dataset

<div class="row mt-3" align="center">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-0" src="{{ site.baseurl }}/assets/img/CRV/dataset-collage.png">
    </div>
</div>
<div class="caption">
    Custom Synthia dataset with plane instance annotations and normal maps.
</div>

##### Overview

[The Synthia dataset](https://synthia-dataset.net/) includes RGB images, depth maps, camera poses, and semantic segmentation maps of synthetic city scene image sequences. However, due to the unavailability of plane instance segmentation and normal maps in Synthia, we have manually annotated the plane instances for a subset of the dataset (`Synthia-Summer-Seq-04`). Using these plane instance annotations, for each plane, we randomly choose three pixels on the plane and convert them to 3D camera points using the corresponding depth map and camera matrix. Subsequently, we use the three 3D points to obtain normal and depth values for each plane.

This dataset comprises 2020 city scene RGB images, normal maps, and segmentation masks of size 1280 x 760 with 1620 training and 400 testing samples. 

#### Resources

- [Dataset](https://drive.google.com/drive/folders/1rF_M7lUy8r8sNRxL201NR5lG23MK2jKv?usp=sharing)
- [Code](https://github.com/mukulkhanna/BF2NormalNet/)


##### Acknowledgement

We thank [Shivaan Sehgal](https://in.linkedin.com/in/shivaan-sehgal-6864991aa) and [Sidhant Subramanian](https://www.linkedin.com/in/sidhant-subramanian-02a90514a) for preparing the manual annotations.