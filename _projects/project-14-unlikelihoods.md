---
number: 14 # leave as-is, maintainers will adjust
title: Bayesian optimization of likely negative candidates in imbalanced biological datasets
topic: real-world
team_leads:
  - <a href="https://github.com/maykcaldas">Mayk Caldas Ramos</a> (University of Rochester)
  - <a href="https://github.com/mehradans92">Mehrad Ansari</a> (Acceleration Consortium)
  - <a href="https://github.com/smichtavy"> Shane Michtavy</a> (University of Rochester)

# Comment these lines by prepending the pound symbol (#) to each line to hide these elements
# contributors:
#   - Contributor 1 (Institution 1)
#   - Contributor 2 (Institution 2)

github: mehradans92/BO-PU
# youtube_video: <your-video-id>
---

Available peptide datasets often lack class balance due to experimental and technical challenges of the high-throughput screening methods in identifying negative examples, which limits the effectiveness of machine learning (ML) models trained on these datasets. A promising solution involves exclusively leveraging positive examples. This method, known as positive-unlabeled (PU) learning[1], treats all non-positive examples as "unlabeled". The classifier is trained by iteratively identifying likely negative candidates (reliable negatives) within the unlabeled data. In this project, we aim to enhance this approach by incorporating Bayesian Optimization (BO)[2,3] for a more strategic selection of likely negative peptide candidates for different biological tasks, including hemolysis and binding against SHP-2 protein target. Utilizing BO to optimize the peptide sequences selection could significantly improve the method's efficiency and accuracy. This is achieved by systematically exploring the example space to find the optimal PU split for training, offering a strategic advantage over traditional heuristic-based methods.[4]

References:
1. Ansari, Mehrad, and Andrew D. White. 2023. [Learning Peptide Properties with Positive Examples Only](https://doi.org/10.1101/2023.06.01.543289) bioRxiv : The Preprint Server for Biology, June.
2. Frazier, Peter I. 2018. [A Tutorial on Bayesian Optimization](http://arxiv.org/abs/1807.02811). arXiv \[stat.ML\]. arXiv
3. Shahriari, Bobak, Kevin Swersky, Ziyu Wang, Ryan P. Adams, and Nando de Freitas. 2016. [Taking the Human out of the Loop: A Review of Bayesian Optimization](https://doi.org/10.1109/JPROC.2015.2494218). Proceedings of the IEEE 104 (1): 148–75.
4. Wang, Ke, and Alexander W. Dowling. 2022. [Bayesian Optimization for Chemical Products and Functional Materials](https://doi.org/10.1016/j.coche.2021.100728). Current Opinion in Chemical Engineering 36 (100728): 100728.
