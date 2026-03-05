---
layout: page
title: AI-Generated Video Detection
description: End-to-end pipeline for detecting AI-generated videos with 99%+ accuracy across Sora, Runway AI, Stable Video Diffusion, and NeRF-based systems. Published at CVPR 2024.
img: assets/img/projects/video_detection.png
importance: 2
category: research
---

## Overview

While deepfake detection research has focused heavily on images, AI-generated **videos** present a fundamentally different forensic challenge. Generators like Sora, Runway AI, and Stable Video Diffusion introduce traces that are qualitatively different from image generators — and existing image detectors fail to catch them.

## Approach

We engineered an end-to-end detection pipeline that exploits **temporal inconsistencies** and **generator-specific forensic artifacts** unique to video generation. The system uses CNNs with temporal forensic analysis to identify AI-generated content across multiple generative architectures.

## Dataset

We constructed and released a large-scale benchmark dataset of **8M+ frames** spanning:

- Transformer-based generators (Sora)
- Diffusion-based generators (Runway AI, Stable Video Diffusion)
- NeRF-based systems

Hosted on **Hugging Face** with 400+ community downloads and adopted by external research groups for benchmarking.

## Results

- **99%+ accuracy** across 4 major generator families
- Robust detection after H.264 re-compression
- Few-shot learning enables detection of new generators with minimal examples

## Impact

- Published at **CVPR Workshops 2024**
- Dataset adopted by external research groups
- 400+ Hugging Face downloads
