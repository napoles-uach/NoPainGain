---
number: 9
title: Optimizing The CO2 Adsorption Capacity of Metal-Organic Frameworks Using Thompson Sampling
topic: general
team_leads:
  - Ray Zhu (University of Chicago)

contributors:
  - Oliver Tang (University of Chicago)
  - Nilesh Jain (Notsohuman.ai)
  - Suraj Sudhakar (University of Chicago)
  - Jaehee Park (University of Chicago)
  - Rija Ansari (National Research Council)

github: AC-BO-Hackathon/real-world-pme-no-hikari
# youtube_video: [Youtube_Video_ID]

---

In this work, we will investigate the optimal selection strategy to find top MOF candidates for carbon capture.
We will adopt the CRAFTED MOF dataset and build Bayesian models with Thompson sampling acquisition function to perform candidate selection.
We will also perform dimension reduction the featurized dataset to optimize the input for surrogate model training, and benchmark Thompson sampling against other acquisition functions to compare their performance in finding top MOF candidates at different adsorption pressures.

References:

1. Oliveira, Felipe Lopes, et al. "CRAFTED: An exploratory database of simulated adsorption isotherms of metal-organic frameworks." Scientific Data 10.1 (2023): 230.
