---
number: 24 # leave as-is, maintainers will adjust
title: ScattBO Benchmark - Bayesian optimisation for materials discovery
topic: benchmark-dev
team_leads:
  - Andy S. Anker (Technical University of Denmark & University of Oxford)


# Comment these lines by prepending the pound symbol (#) to each line to hide these elements
contributors:
  - Samuel Ampofo Appiah (Ghana National Gas Company)

# github: AC-BO-Hackathon/project-ScattBO
# youtube_video: <your-video-id>

---

A self-driving laboratory (SDL) is an autonomous platform that conducts machine learning (ML) selected experiments to achieve a user-defined objective. An objective can be to synthesise a specific material.[1]
Such an SDL will synthesise a material, evaluate if this is the target material and if necessary optimise the synthesis parameters for the next synthesis. One way to evaluate if the material is the target material is by measuring scattering data and comparing that to the scattering pattern of the target material.

Here, we present a Python-based benchmark (ScattBO) that simulates a SDL for materials discovery. Based on a set of synthesis parameters, the function "synthesis" a structure, calculate the scattering pattern[2] and compare this to the scattering pattern of the target structure. Note: Scattering data may not be enough to definitely validate that the target material has been synthesised.[3] The benchmark can include other types of data as long they can be simulated.

More documentation and scoreboard can be found at https://github.com/AndySAnker/ScattBO/tree/main.

**References**:

[1] Szymanski, Nathan J., et al., An autonomous laboratory for the accelerated synthesis of novel materials, Nature, 624(7990), 86-91 (2023)

[2] Frederik L. Johansen & Andy S. Anker, et al., A GPU-Accelerated Open-Source Python Package for Calculating Powder Diffraction, Small-Angle-, and Total Scattering with the Debye Scattering Equation, Journal of Open Source Software, 9(94), 6024 (2024)

[3] Leeman, Josh, et al., Challenges in High-Throughput Inorganic Materials Prediction and Autonomous Synthesis, PRX Energy, 3(1), 011002 (2024)
