# Airline Hub Optimization with Demand and Sensitivity Analysis

## Overview
This repository contains two versions of a mathematical modeling project optimizing airline hub locations for Short-Hop Airline across nine cities. The goal is to minimize hubs while ensuring all cities are within 200 miles of a hub and accounting for passenger demand. This work originated as a case study for a Math research course at the University of Alberta, reconstructing a cost-efficient airline hub and network business model. The original paper (2021) has been revised and expanded in 2025 with advanced methods, and I’ve decided to make it open-source to share with the community.

- **Revised Paper (2025)**: Uses Integer Linear Programming (ILP), dominating sets, and spectral graph theory to identify Green Bay (GB), South Bend (SB), and Fort Wayne (F) as optimal hubs, with sensitivity analysis for robustness.
- **Old Paper (2021)**: An earlier version with simpler assumptions, focusing on distance-based optimization.

## Files
- **revised_2025/paper.tex**: LaTeX source for the 2025 revised paper.
- **revised_2025/paper.pdf**: Compiled PDF (if compiled).
- **old_2021/old_paper.tex**: LaTeX source for the 2021 original paper.
- **old_2021/old_paper.pdf**: Compiled PDF (if compiled).
- **figures/**: Placeholder directory for figures:
  - `distance_matrix.tex` (optional): TikZ or image for Figure 1 (distance matrix, not fully included due to missing data).
  - `network_graph.tex`: Embedded in `revised_2025/paper.tex` as Figure 2 (TikZ network graph).
  - `sensitivity_plot.tex`: Embedded in `revised_2025/paper.tex` as Figure 3 (TikZ sensitivity plot).
- **README.md**: This file.

## Requirements
- LaTeX distribution (e.g., TeX Live, MiKTeX) with packages: `amsmath`, `amssymb`, `graphicx`, `booktabs`, `geometry`, `tikz`.
- Optional: Python/Matplotlib for alternative figure generation (see below).

## Compilation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/airline-hub-optimization.git
