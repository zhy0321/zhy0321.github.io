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

## Contributions

1. Observing the unstable learning caused by inconsistent and incorrect pseudo labels, we propose a novel spatial-temporal
consistency framework for SSCC. It combines temporal feature consistency of the same density level and spatial consistency of different views for the same
image to leverage unlabeled images.

2. To realize temporal consistency, we design a simple yet effective dynamic temporal knowledge memory, which
stores temporal features of images with different density levels. It can reduce the negative impact of inconsistent optimization targets on model performance.

3. Using an uncertainty-aware teacher, we present a pseudolabel filtering mechanism. It can prevent incorrect pseudo
labels from degrading model training, by reducing the supervision weights of unreliable pseudo labels with high uncertainty.

## The Proposed Framework

<div align="middle"><img align="middle" style="max-width: 800px; width: 100%" src="https://KingMV.github.io/files/STC_Crowd_Framework.jpg" /></div>

Our framework is based on the teacher-student architecture. We design a DTKM module and a PLF mechanism to improve model performance under the SSL setting.
The DTKM preserves the teacher’s temporal encoding features of various density levels during training so that the student’s features in the current stage are encouraged to be consistent with its previous temporal features. The PLF mechanism is used to reduce the supervision weights of unreliable pseudo labels with high uncertainty. The uncertainty is acquired from a diverse set of predictions for an image by the Masksembles, which mainly inserts a feature mask layer into the crowd counting model. The optimization objective consists of supervised loss and unsupervised loss.

## Experiment Results

Comparison results on various crowd datasets:

![](https://KingMV.github.io/files/STC_Crowd_performance.jpg)


Visualization examples from different crowd counting datasets (e.g. SHHB, SHHA, QNRF, JHU-Crowd++, NWPU-Crowd). 

![](https://KingMV.github.io/files/STC_Crowd_vis.jpg)
