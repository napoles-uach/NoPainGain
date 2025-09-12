---
number: 37 # leave as-is, maintainers will adjust
title: Embedding System Knowledge into Bayesian Optimizers
topic: general
team_leads:
  - Thomas Andrews (The University of Melbourne, CSIRO)

# Comment these lines by prepending the pound symbol (#) to each line to hide these elements
# contributors:
#  - Contributor 1 (Institution 1)
#  - Contributor 2 (Institution 2)

# github: AC-BO-Hackathon/<your-repo-name>
# youtube_video: <your-video-id>

---

Bayesian optimization is often considered a black-box technique, however several simple modifications to the design can vastly increase the optimizers computational and iterative performance on certain tasks. Two such modifications will be explored in this work; post-modelling objective computation for enhanced computational efficiency and improved knowledge integration, and minimum length-scale enforcement for increased stability of optimizers to system noise when using homoscedastic noise modelling.

Post-modelling objective computation often reduces the number of models that need be fitted to the data and can result in them having a more representative posterior as the transformations created by the formulating the objectives can be decoupled from the raw measurement values.

Bayesian optimizers utilizing homoscedastic noise modelling must balance both fitting of both the kernels and the noise. Methods optimizing the marginal likelihood are prone to overfitting the kernels during early iterations leading to suboptimal algorithm performance. This is due to the presence of a second optima in the marginal likelihood curve with respect to length-scale which occurs when the model stops explaining the system noise with the fitted kernels and instead begins correctly capturing it in the inferred system noise. Providing a minimum length-scale can help locate this secondary optima and ensure that the kernels only capture the base trends and not the system noise. 

The impacts of these modifications on computational and iterative performance will be demonstrated using the optimization of a simulated nucleophilic aromatic substitution reaction system. This simulated system was adapted from the summit software package<sup>1</sup> and is based on the works of Hone et al.<sup>2</sup>.

References:
1. Felton, K. C., Rittig, J. G., & Lapkin, A. A. (2021), [Summit: benchmarking machine learning methods for reaction optimisation](https://doi.org/10.1002/cmtd.202000051). _Chemistry‐Methods_, _1_(2), 116-122.
2. Hone, C. A., Holmes, N., Akien, G. R., Bourne, R. A., & Muller, F. L. (2017). [Rapid multistep kinetic model generation from transient flow data](https://doi.org/10.1039/C6RE00109B). _Reaction chemistry & engineering_, _2_(2), 103-108.
