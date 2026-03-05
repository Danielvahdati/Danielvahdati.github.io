---
layout: page
title: Real-Time Puppeteering Defense
description: First enrollment-free defense against identity puppeteering in AI-based videoconferencing. 97.7% AUC at 75 FPS. Published at NeurIPS 2025 in collaboration with NVIDIA Research.
img: assets/img/projects/puppeteering_defense.png
importance: 1
category: research
---

## Overview

AI-based videoconferencing systems reduce bandwidth by transmitting a compact pose-expression latent and re-synthesizing video at the receiver. This architecture is vulnerable to **puppeteering attacks**, where an adversary hijacks a victim's likeness in real time by injecting a malicious latent stream.

Because every frame is synthetic, standard deepfake detectors fail outright — the video is always fake by design. We needed a fundamentally different approach.

## Key Insight

The pose-expression latent inherently leaks biometric information about the **driving identity** — the person actually controlling the face. We exploit this leakage to detect identity mismatches without ever looking at the reconstructed RGB video.

## Approach

We introduce a **pose-conditioned large-margin contrastive loss (PC-LMCL)** that trains an encoder to isolate persistent identity cues inside the transmitted latent while cancelling transient pose and expression variation. A simple cosine similarity test on this disentangled embedding flags illicit identity swaps in real time.

## Results

- **97.7% AUC** at **75 FPS** — fast enough for real-time deployment
- **46% error reduction** over prior state-of-the-art
- Strong generalization to unseen systems (AUC 0.925 cross-domain)
- No enrollment data required

## Impact

- Published at **NeurIPS 2025** (main conference)
- Collaboration with **NVIDIA Research** (Ekta Prashnani, Koki Nagano, Orazio Gallo)
- Secured **$150K NVIDIA research gift** and 1 year of dedicated compute
