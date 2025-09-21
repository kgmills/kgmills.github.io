---
title: "Re-ttention Accepted to NeurIPS'25"
date: 2025-09-18 09:00:00 -0500
categories: publications neurips academic
layout: single
author_profile: true
---

I am very happy to report that our paper "Re-ttention: Ultra Sparse Visual Generation via Attention Statistical Reshape" has been accepted to NeurIPS 2025!

Re-ttention achieves extreme attention sparsity on Text-to-Video (T2V) and Text-to-Image (T2I) Diffusion Models by leveraging the iterative denoising process to cache and re-use attention information. Specifically, we observe the crucial role that the denominator term of the softmax operation plays in ensuring high-quality visual generation and design our method around this criticality. In doing so we are able to achieve ultra-sparse attention by denominator rescaling across denoising time-steps as well as residual caching between the full-attention and sparse attention.

The end result is that we are able to reduce the number of attention tokens down to 3.1% of the original number and still achieve quality visual generation on models such as CogVideoX and PixArt-Σ.

The speed and throughput of the AI/ML community is reaching levels akin to ["ludicrious speed" from Spaceballs (1987)](https://www.youtube.com/watch?v=NAWL8ejf2nM) . NeurIPS, in particular, the top conference for AI/ML research, is extremely competitive this year, with over 25k paper submissions, over 21.5k after desk rejection, and almost 5.3k accepted papers for an overall accept rate of 24.52%. In fact, the conference is expanding from San Diego into Mexico City and Copenhagen, Europe through "EurIPS".

I am impelled to give thanks and a shout-out to my co-authors, especially [Ruichen Chen](https://scholar.google.com/citations?user=WHiR96wAAAAJ&hl=en&oi=ao), [Liyao Jiang](https://scholar.google.com/citations?user=OSpqcyoAAAAJ&hl=en), [Dr. Chao Gao](https://cgao3.github.io/) and my former advisor, [Professor Di Niu](https://sites.ualberta.ca/~dniu/Homepage/Home.html) from the Department of Electrical and Computer Engineering at the University of Alberta! Very grateful to have had the pleasure of working with you on this collaboration! 

<p align="center">
    <img src="/images/Rettention_sloth_thumbnail.png" width="400" alt="Rettention Sloth Thumbnail">
</p>

**Note:** This is a copy of my [LinkedIn post](https://www.linkedin.com/feed/update/urn:li:activity:7374569785222885376/) on this announcement. 