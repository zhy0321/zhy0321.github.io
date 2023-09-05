---
title: "Semi-supervised Crowd Counting with Spatial Temporal Consistency and Pseudo-label Filter"
collection: publications
permalink: /publications/stc_crowd
excerpt: 'The performance of semi-supervised crowd counting (SSCC) can be significantly improved by reducing the over-fitting of the
incorrect pseudo labels. This paper proposed a novel spatial-temporal consistency framework, named STC-Crowd.'
date: 2023-08-04
venue: 'IEEE TCSVT'
---

[paper](https://ieeexplore.ieee.org/abstract/document/10032602){: .btn .btn--info}

## Abstract

Semi-supervised crowd counting (SSCC) aims to learn a crowd counting model with limited labeled images and a large number of unlabeled images. Previous works leverage unlabeled images by pseudo-labeling and spatial consistency regularization paradigms, which frequently adopt teacher-student frameworks. However, their performances are readily degraded due to the inconsistent and unreliable pseudo density map in complex crowd scenes. Here, we argue that the SSCC performance can be significantly improved by reducing the over-fitting of the incorrect pseudo labels, and a novel spatial-temporal consistency framework, named STC-Crowd, is proposed. Under different spatial perturbations, spatial consistency enables the counting model to output consistent predictions for the same crowd image. Temporal consistency generates similar feature embedding over adjacent training stages, alleviating the inconsistent issues of pseudo density maps generated for the same image over time. To store the temporal feature embedding of different density levels for temporal consistency, a dynamic temporal knowledge memory (DTKM) is deliberately designed, and considerably reduces the storage cost. Besides, a pseudo-label filter (PLF) mechanism is used to alleviate the negative impact of incorrect pseudo density maps, by reducing the supervision weights of unreliable pseudo labels with high uncertainty. Extensive experiments on four benchmark datasets show that our method obtains competent performance against leading SSCC methods, and especially works
better on limited labeled images.

## The Proposed Framework

<div align="middle"><img align="middle" style="max-width: 800px; width: 100%" src="https://KingMV.github.io/files/STC_Crowd_Framework.jpg" /></div>

