---
number: 29 # leave as-is, maintainers will adjust
title: A Bayesian Approach to Predict Solubility Parameters
topic: general
team_leads:
  - Johannes Poms (RCPE)

# github: AC-BO-Hackathon/project-solubility

---

The critical role of solubility spans numerous domains, affecting everything from liquid miscibility and polymer stability to solid adsorption. 
This phenomenon's accurate and swift prediction can significantly advance a variety of industries, including organic semiconductors, paint coatings, pharmaceuticals, and every chemical synmthesis. 
However, the challenge in predicting solubility lies in the complex interplay between the solute and solvent, compounded by a myriad of other physical and chemical properties. This complexity underscores the need for advanced methodologies that can navigate the intricacies of solubility, thereby enabling better material design and formulation across multiple fields.

In [1] Gaussian Process Modeling was proposed to predict the Hansen solubility parameter from chemical descriptors and sigma profiles. However, not the complete code of the implementation of the paper was provided, but it includes a huge dataset and can serve as benchmark.  
Recently, GAUCHE [2] was released, a framework for gaussian processes in chemistry. It builds on top of gpytorch, which gives it the GPU computation ability of Torch and Bayesian optimization implemented in botorch. It includes the interfaces to over 30 kernels, including kernels specific for molecular fingerprints.

The goal of the project is to implement Gaussian Process Modeling for the dataset and compare the performance of different kernels.


References:

1. Sanchez-Lengeling, Roch, Perea, Langner, Brabec, Aspuru-Guzik (2018), ["A Bayesian Approach to Predict Solubility Parameters"](http://doi.org/10.1002/adts.201800069), Advanced Theory and simulations: Vol. 2: Issue 1.

2. Griffiths et al. [GAUCHE: A Library for Gaussian Processes in Chemistry](https://neurips.cc/virtual/2023/poster/70081)https://neurips.cc/virtual/2023/poster/70081). Poster. https://github.com/leojklarner/gauche
