---
layout: page
title: Low-Bandwidth Puppeteering Defense
description: First defense against puppeteering attacks in low-bandwidth talking head videoconferencing systems. 98.03% detection accuracy. Published at CVPR 2023.
img: assets/img/projects/lowbandwidth_defense.png
importance: 5
category: research
---

## Overview

Low-bandwidth talking head videoconferencing systems compress video by transmitting facial pose and expression vectors instead of raw frames, reconstructing video at the receiver. This architecture is highly vulnerable to **puppeteering attacks** — an attacker can substitute their own pose/expression vectors to control the target's synthesized face in real time.

At the time of this work, no defenses existed against this attack vector.

## Approach

We exploit biometric information inherently present in the transmitted pose and expression vectors. Even though these vectors are designed to capture motion, they also encode identity-specific characteristics of the person generating them. We use this leakage to verify that the driving identity matches the enrolled speaker.

The system requires **no modifications** to the video transmission pipeline and operates with low computational overhead.

## Results

- **98.03% detection accuracy** across 4 distinct talking head systems
- Real-time operation compatible with live videoconferencing
- New benchmark dataset released for evaluating puppeteering defenses

## Impact

- Published at **CVPR Workshops 2023**
- Foundational work that led to the more advanced NeurIPS 2025 system
