# Temporal autocorrelation increases temperature-driven extinction risk by clustering stressful conditions
Climate change affects the thermal environment in complex ways, including changing its temporal autocorrelation structure and intensifying heatwave regimes. While theory shows that higher temporal autocorrelation may exacerbate extinction risks, little work has been done to incorporate autocorrelation into thermal performance-based forecasting. Here, we pair stochastic simulation models of population dynamics with systematically generated temperature time series to determine when increasing the temporal autocorrelation of variable thermal environments generates greater extinction risks. We show that by clustering stressful conditions, increasing autocorrelation reduces the extent of warming and variability which populations with unimodal thermal tolerance can survive. We validate our predictions with a factorial experiment in protist microcosms, where we find that higher autocorrelation significantly elevates extinction risk when environments include stressful temperatures. Taken together, these results provide the foundation for predicting which species and environments face the greatest thermal risks under increasing autocorrelation.

Released 7/2025. Updated 11/2025.

## Sections

### Methods figures ('MethodsFigures.nb')
This code generates Fig 1 and 2 from the 'Materials & Methods' section. It can also be used to generate new temperature time series with specified thermal distributions and levels of autocorrelation. Before recreating the figures in the paper, you will need to download 'PcaudatumTPCdata.csv'.

### Forecasting extinction risk under temporal autocorrelation ('ForecastingRisk.nb')
This code generates Fig 4 using an SDE population dynamic model. For fast figure replication, download the requisite simulation results first (all 'SDE...m' and 'windowing...m' files; windowing files are large and will need to be unzipped).

### Experimental Results and SSA Simulations ('SSAandExperiments.nb')
This code generates Fig 5 using an SSA population dynamic model and compares simulation outcomes to experimental results. For fast replication, download the requisite simulation results first (all 'SSA2...m' files). This file additional contains the code needed to plot experimental outcomes as shown in the Supplemental Material; before recreating these figures, you will need to download 'experimentalresults.csv'.

### TPC Fitting ('rTPCs_curvefitting.Rmd')
This file fits TPCs to the experimental data using the 'rTPC' R package.

### Statistics ('AutocorrExperimentStats.Rmd')
This file computes all used statistics, including fitting experimental results to a bias-reduced linear regression model (requires brglm package), computing chi-squared tests, and conducting posthoc pairwise comparisons (requires emmeans package); described in depth in Supplement S5.

## References
Lactin, D.J, N.J. Holliday, D.L. Johnson, and R. Craigen. ["Improved Rate Model of Temperature-Dependent Development by Arthropods."](https://academic.oup.com/ee/article-abstract/24/1/68/2394752) Environmental Entomology 24(1): 68-75.

Robey, A.J., M.T. Kummel, and D.A. Vasseur. ["Temporal autocorrelation increases temperature-driven extinction risk."](https://doi.org/10.1101/2025.07.29.667527).

Robey, A.J. and D.A. Vasseur. ["Order matters: Autocorrelation of temperature dictates extinction risk in populations with nonlinear thermal performance."](https://doi.org/10.1101/2024.12.19.629491) In review. ([Code available here](https://github.com/arobey63/autocorrelation))

Vasseur, D.A., C. Bieg, M.T. Kummel, and A.J. Robey. ["Forecasting Extinction Risk using Thermal Performance Curves and Population Dynamic Modeling."](https://doi.org/10.1101/2025.04.27.650737) In review. ([Code available here](https://github.com/dvasseur9/Forecasting-Extinction-Risk))
