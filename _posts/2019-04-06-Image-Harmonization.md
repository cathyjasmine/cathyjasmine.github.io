---
title: Image Harmonization
date: 2019-04-06 13:12:12
tags: [Deep Learning, Image Harmonization, GAN]
categories: Paper Note
---

### Traditional Harmonization Methods

Histogram Matching

CG2Real: Improving the Realism of Computer Generated Images Using a Large Collection of Photographs 

1. use **co-segmentation** to segment and match regions in a single step .the content of all images is taken into account during co-segmentation and matching regions are automatically produced as a byproduct  of  [1]

   [1] **Cosegmentation of Image Pairs by Histogram Matching- Incorporating a Global Constraint into MRFs **

2. mean-shift framework [2]

   [2] **The Estimation of the Gradient of a Density Function, with Applications in Pattern Recognition **

   3. feature vector: concatenation of the pixel color in L* a* b* space, the normalized x and y coordinates at p, and a binary indicator vector (i0; . . . ; ik) such that ij is 1 when pixel p is in the jth image and 0 otherwise 
   4. a combination of joint-bilateral up-sampling and local color transfer

### related topics

- **alpha matting**: Fuse image by combining their absolute pixel values. The color of the image are linearly interpolated using weights specified by the alpha matte.
- gradient domain compositing
- image blending
  - Poisson blending
- image pyramids
  - Laplacian pyramids 