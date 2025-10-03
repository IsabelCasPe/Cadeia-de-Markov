<!-- HERO -->
# Art & Science in Motion - Living Mathematics. 💎✨
[![USP](https://img.shields.io/badge/USP-Dissertação-0A3D91?logo=academia&logoColor=white)](https://teses.usp.br/teses/disponiveis/3/3151/tde-20102010-122044/en.php)
[![arXiv](https://img.shields.io/badge/arXiv-2504.01969-B31B1B?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2504.01969)
![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![License](https://img.shields.io/badge/License-MIT-gold)
![Made with ❤](https://img.shields.io/badge/Made%20with-❤-ff69b4)

**PT · EN · ES** · [Galeria](#galeria--gifs) · [Instalação](#instalação--installation--instalación) · [Licença MIT](#licença--license--licencia)

---
## Markov-Chains-Study
*(Alias: Cadeias-de-Markov)*    
A Personal Exploration of Markov Chains        

This repository contains study materials, code examples, and explorations of Markov Chains and stochastic processes, inspired by *Markov Chains and Mixing Times* by Levin, Peres, and Wilmer (2009) and other sources. The goal is to deepen understanding of advanced topics and their applications in modern research.

## Contents 

- [Introduction to Markov Chains](#introduction-to-Markov-Chains-and-their-properties) 
- [Transition Matrices](#transition-matrices)
- [Classification of States](#classification-of-states)
- [Steady-State Behavior](#steady-state-behavior)
- [Advanced Topics and Applications](#advanced-topics-and-applications)
- [Solved Exercises](#solved-exercises)
- [Additional References and Resources](#additional-references-and-resources)

## Objective

This project aims to explore theoretical and practical aspects of Markov Chains, bridging probability and linear algebra to support personal research and applications in stochastic processes, optimization, and machine learning. It reflects a self-directed study inspired by academic literature.

## Course Outline

The study is divided into two parts:

### Part 1: Foundations
- Introduction to Markov Chains and their properties.
- Construction and analysis of transition matrices.
- Classification of states (transient, recurrent, absorbing).
- Convergence to steady-state behavior and stationary distributions.

### Part 2: Advanced Topics and Applications
- Mixing times and convergence rates.
- Coupling methods and comparison techniques.
- Applications in statistical physics, network analysis, and machine learning.
- Hands-on projects and simulations.

## Prerequisites

- Familiarity with elementary probability concepts (e.g., Chapter 1 of *Probability: An Intermediate Course* by Barry James).
- Some knowledge of linear algebra and/or elementary algebra is advisable but not essential.

## Implementation

### Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/IsabelCasPe/Markov-Chains-Study.git
## References

- [IMPA Official Website](https://impa.br/)
- Additional materials are cited within the repository.

## Inspiration.
> **"In the transitions of chance, Markov chains weave the quantum future — @CadeiaDeMarkov where stochastic chaos meets the dance of probabilities!"** 🎲
>  Copyright © 2025 Prof. Ana Isabel C. 💙

---
## © 2025 Ana Isabel Castillo Pereda — All rights reserved.
This repository or portions thereof may not be reused, redistributed, or forked without explicit permission from the author. For reuse requests, contact: anacp20@gmail.com
---
## © 2025 Ana Isabel Castillo Pereda — Todos os direitos reservados.
Este repositório ou partes dele não podem ser reutilizados, redistribuídos ou bifurcados sem a permissão explícita da autora. Para solicitações de reutilização, entre em contato com: anacp20@gmail.com
---


mkdir -p gifs/wm_out
for f in gifs/*.gif; do
  base=$(basename "$f" .gif)
  ffmpeg -i "$f" -i watermark.png \
    -filter_complex "overlay=main_w-overlay_w-10:main_h-overlay_h-10" \
    -c:v libvpx-vp9 -b:v 0 -crf 30 -y "gifs/wm_out/${base}.webm"
done


mkdir -p gifs/wm_out
for f in gifs/*.gif; do
  base=$(basename "$f" .gif)
  magick "$f" -coalesce -gravity southeast -fill "rgba(255,255,255,0.5)" \
    -pointsize 20 -annotate +10+10 "© IsabelCasPe" -layers Optimize "gifs/wm_out/${base}_wm.gif"
done
