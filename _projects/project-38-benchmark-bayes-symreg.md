---
number: 38 # leave as-is, maintainers will adjust
title: Benchmarking Bayesian Symbolic Regression
topic: general
team_leads:
  - Cher-Tian Ser (University of Toronto)
  - Sergio Pablo-Garcia (University of Toronto)
  - Shi Xuan Leong (University of Toronto)
  - Marko Huang (University of Toronto)
  - Andrew Wang (University of Toronto)

# Comment these lines by prepending the pound symbol (#) to each line to hide these elements
contributors:

# github: AC-BO-Hackathon/bayes-pysr-benchmark
# youtube_video: <your-video-id>

---

This project investigates the use of Bayesian methods in symbolic regression for use in the physical sciences. Symbolic regression (SR) is a machine learning approach that aims to obtain an analytical mathematical expression to fit a dataset, through optimizing the mathematical operations and coefficients within the expression. The interpretability of these expressions make it attractive for deployment across multiple use cases, including the derivation of physical laws. State-of-the-art SR methods involve the use of genetic programming (or genetic algorithms) to construct such functions, which are unable to incorporate expert knowledge and are thus inefficient in its sampling of mathematical expressions. While a Bayesian version of symbolic regression was proposed and implemented to replace the genetic component of expression construction [1], its performance on the general symbolic regression benchmark SRBench was poor [2]. However, its performance on a physical-science focused symbolic regression benchmark SRSD [3] was not evaluated. Our goal is to evaluate how SR can be enhanced using Bayesian methods to achieve better performance in the discovery of analytical expressions for the physical sciences.

References:
[1]	Y. Jin, W. Fu, J. Kang, J. Guo, and J. Guo, “Bayesian Symbolic Regression.” arXiv, Jan. 15, 2020. doi: 10.48550/arXiv.1910.08892.
[2]	W. La Cava et al., “Contemporary Symbolic Regression Methods and their Relative Performance.” arXiv, Jul. 29, 2021. doi: 10.48550/arXiv.2107.14351.
[3]	Y. Matsubara, N. Chiba, R. Igarashi, and Y. Ushiku, “Rethinking Symbolic Regression Datasets and Benchmarks for Scientific Discovery.” arXiv, Mar. 05, 2024. Accessed: Mar. 26, 2024. [Online]. Available: http://arxiv.org/abs/2206.10540
