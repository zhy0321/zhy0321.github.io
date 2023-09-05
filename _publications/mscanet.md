---
title: "Multi-scale context aggregation network with attention-guided for crowd counting"
collection: publications
permalink: /publication/MSCANet
excerpt: 'This paper is about the number 2. The number 3 is left for future work.'
date: 2020-12-01
venue: '15-th IEEE International Conference on Signal Processing'
---
This paper is about the number 2. The number 3 is left for future work.

[paper](https://ieeexplore.ieee.org/abstract/document/9321067) {: .btn .btn--info}
[code](https://github.com/KingMV/MSCANet){: .btn .btn--info}

## Abstract 
Crowd counting aims to predict the number of people and generate the corresponding density map in the image.
There are many challenges, including varying head scales, the diversity of crowd distribution across images, and cluttered backgrounds. In this paper, we propose a multi-scale context aggregation network (MSCANet) based on single-column encoder-decoder architecture for crowd counting, which consists of an encoder based on a dense context-aware module (DCAM) and a hierarchical attention-guided decoder. To handle the issue of scale variation, we construct the DCAM to aggregate multiscale contextual information through densely connecting the dilated convolution with varying receptive fields. The proposed DCAM can capture rich contextual information of the crowd, due to its long-range receptive fields and dense scale sampling. Moreover, to suppress the background noise and generate a high-quality density map, we adopt a hierarchical attention-guided mechanism in the decoder. This helps to integrate more
useful spatial information from shallow feature maps of the encoder by introducing multiple supervision based on semantic attention modul (SAM). Extensive experiments demonstrate that the proposed approach achieves better performance than other similar state-of-the-art methods on three challenging benchmark datasets for crowd counting.

## Contributions

1. We propose a multi-scale context aggregated network based on the encoder-decoder architecture for crowd counting. A dense context-aware module (DCAM) is designed to capture rich contextual information and large-range scale information through densely connecting multiple dilated kernels with different receptive fields.

2. We design a hierarchical attention-guided decoder to explicitly integrate important information of different levels of feature maps from the encoder, which can obtain a high-quality density map. Multiple SAMs are introduced into different stages of the decoder to make the shallow feature maps of crowd areas get more attention.


## Overview Framework

![](https://KingMV.github.io/files/mscanet_framework.png)


The backbone based on VGG16 is used to extract the basic visual feature representation of an input image. Then these features are fed into multiple dense context-aware modules (DCAM) to enhance the representation of multi-scale features. Each DCAM aggregates contextual information from different receptive fields through densely connecting dilated convolution of different dilated rates. The hierarchical attention-guided decoder is used to explicitly integrate important information of different encoded feature maps.
