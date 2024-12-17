---
title: "SPPNet: A Single-Point Prompt Network for Nuclei Image Segmentation"
collection: publications
category: conferences
link: /publications/SPPNET
permalink: https://doi.org/10.48550/arXiv.2308.12231
excerpt: 'Image segmentation plays an essential role in nuclei image analysis. Recently, the segment anything model has made a significant breakthrough in such tasks. However, the current model exists two major issues for cell segmentation: (1) the image encoder of the segment anything model involves a large number of parameters. Retraining or even fine-tuning the model still requires expensive computational resources. (2) in point prompt mode, points are sampled from the center of the ground truth and more than one set of points is expected to achieve reliable performance, which is not efficient for practical applications. In this paper, a single-point prompt network is proposed for nuclei image segmentation, called SPPNet. We replace the original image encoder with a lightweight vision transformer. Also, an effective convolutional block is added in parallel to extract the low-level semantic information from the image and compensate for the performance degradation due to the small image encoder. We propose a new point-sampling method based on the Gaussian kernel. The proposed model is evaluated on the MoNuSeg-2018 dataset. The result demonstrated that SPPNet outperforms existing U-shape architectures and shows faster convergence in training. Compared to the segment anything model, SPPNet shows roughly 20 times faster inference, with 1/70 parameters and computational cost. Particularly, only one set of points is required in both the training and inference phases, which is more reasonable for clinical applications. The code for our work and more technical details can be found at [this URL](https://github.com/xq141839/SPPNet).'
date: 2023-10-10
venue: 'MICCAI-MLMI'
paperurl: 'http://JohnnyZhang728.github.io/files/SPPNet.pdf'
citation: 'Qing Xu, Wenwei Kuang, Zeyu Zhang, Xueyao Bao, Haoran Chen, and Wenting Duan (2023, October). “SPPNet: A
Single-Point Prompt Network for Nuclei Image Segmentation.” In International Workshop on Machine Learning in
Medical Imaging (pp. 227-236). Cham: Springer Nature Switzerland.'
---

The contents above will be part of a list of publications, if the user clicks the link for the publication than the contents of section will be rendered as a full page, allowing you to provide more information about the paper for the reader. When publications are displayed as a single page, the contents of the above "citation" field will automatically be included below this section in a smaller font.
