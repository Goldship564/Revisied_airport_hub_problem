# Airline Hub Optimization with Demand and Sensitivity Analysis

## Overview
This repository contains two versions of a mathematical modeling project optimizing airline hub locations for Short-Hop Airline across nine cities. The goal is to minimize hubs while ensuring all cities are within 200 miles of a hub and accounting for passenger demand. This work originated as a case study for a Math research course at the University of Alberta, reconstructing a cost-efficient airline hub and network business model. The original paper (2021) has been revised and expanded in 2025 with advanced methods, and I’ve decided to make it open-source to share with the community.

- **Revised Paper (2025)**: Uses Integer Linear Programming (ILP), dominating sets, and spectral graph theory to identify Green Bay (GB), South Bend (SB), and Fort Wayne (F) as optimal hubs, with sensitivity analysis for robustness.
- **Old Paper (2021)**: An earlier version with simpler assumptions, focusing on distance-based optimization.

## Files
- **revised_2025/paper.pdf**: Compiled PDF .
- **old_2021/old_paper.pdf**:  PDF.
- **README.md**: This file.

## Requirements
- LaTeX distribution (e.g., TeX Live, MiKTeX) with packages: `amsmath`, `amssymb`, `graphicx`, `booktabs`, `geometry`, `tikz`.
- Optional: Python/Matplotlib for alternative figure generation (see below).
- # sensitivity_plot.py
import matplotlib.pyplot as plt
import numpy as np

C_h = np.linspace(0, 100000, 100)
Z_2 = 2 * C_h + 94750
Z_3 = 3 * C_h + 73050

plt.plot(C_h, Z_2, 'b-', label='Two Hubs (GB, SB)')
plt.plot(C_h, Z_3, 'r-', label='Three Hubs (GB, SB, F)')
plt.axvline(21700, color='k', linestyle='--', label='Threshold: $C_h = 21,700$')
plt.xlabel('Fixed Hub Cost $C_h$ (dollars/day)')
plt.ylabel('Total Cost $Z$ (dollars/day)')
plt.legend()
plt.grid(True)
plt.savefig('sensitivity.png')
plt.show()

## Compilation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/airline-hub-optimization.git
