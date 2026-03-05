---
layout: page
title: GAN Face Detection via Semantic Inconsistencies
description: GAN-generated face detector leveraging facial semantic inconsistencies across eyes, mouth, and hair regions. 91.36% accuracy with robustness to JPEG compression. Published at Electronic Imaging 2023.
importance: 6
category: research
---

## Overview

GAN-generated faces appear visually realistic at first glance but often contain subtle **semantic inconsistencies** — misaligned eye highlights, unrealistic hair textures, inconsistent teeth — that are imperceptible to humans but detectable by trained classifiers.

Most existing detectors exploit low-level statistical traces introduced during synthesis. We take a complementary approach: searching for high-level semantic artifacts across specific facial regions.

## Approach

We build a multi-branch detector with specialized CNNs for different facial regions (eyes, mouth, hair), then fuse their outputs via an SVM classifier. This architecture forces the model to look for semantic meaning rather than statistical noise.

## Results

- **91.36% accuracy** on GAN-generated face detection
- Robust to JPEG compression and resizing attacks — outperforms CNN-based statistical detectors under post-processing
- Generalizes across GAN architectures without architecture-specific training

## Impact

- Published at **Electronic Imaging 2023**
