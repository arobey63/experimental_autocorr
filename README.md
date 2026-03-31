# Temporal autocorrelation increases temperature-driven extinction risk by clustering stressful conditions
Climate change affects the thermal environment in complex ways, including changing its temporal autocorrelation structure and intensifying heatwave regimes. While theory shows that higher temporal autocorrelation may exacerbate extinction risks, little work has been done to incorporate autocorrelation into thermal performance-based forecasting. Here, we pair stochastic simulation models of population dynamics with systematically generated temperature time series to determine when increasing the temporal autocorrelation of variable thermal environments generates greater extinction risks. We show that by clustering stressful conditions, increasing autocorrelation reduces the extent of warming and variability which populations with unimodal thermal tolerance can survive. We validate our predictions with a factorial experiment in protist microcosms, where we find that higher autocorrelation significantly elevates extinction risk when environments include stressful temperatures. Taken together, these results provide the foundation for predicting which species and environments face the greatest thermal risks under increasing autocorrelation.

Initial released 7/2025; revised 11/2025; revised 3/2026.

## Sections

### Methods figures ('MethodsFigures.nb')
This code generates Fig 1 and 2 from the 'Materials & Methods' section. It can also be used to generate new temperature time series with specified thermal distributions and levels of autocorrelation (see also Robey et al., 2026). Before recreating the figures in the paper, you will need to download 'PcaudatumTPCdata.csv'.

### Forecasting extinction risk under temporal autocorrelation ('ForecastingRisk.nb')
This code generates Fig 4 and S2-4 using an SDE population dynamic model (see also Vasseur et al., 2025). For fast figure replication, download the requisite simulation results first (all 'SDE...m' and 'windowing...m' files; windowing files are large and will need to be unzipped).

### Experimental Results and SSA Simulations ('SSAandExperiments.nb')
This code generates Fig 6 and S5 using an SSA population dynamic model and compares simulation outcomes to experimental results. For fast replication, download the requisite simulation results first (all 'SSA2...m' files). This file additional contains the code needed to plot experimental outcomes as shown in the Supplemental Material; before recreating these figures, you will need to download 'experimentalresults.csv'.

### TPC Fitting ('rTPCs_curvefitting.Rmd')
This file fits TPCs to the experimental data to the 'lactin2' TPC model (Lactin et al., 1995) using the 'rTPC' R package (Padfield et al., 2024).

### Statistics ('AutocorrExperimentStats.Rmd')
This file computes all used statistics, including fitting experimental results to a bias-reduced linear regression model (requires brglm package), computing chi-squared tests, and conducting posthoc pairwise comparisons (requires emmeans package); described in depth in Supplement S5.

### Code PDFs ('codepdfs')
This file contains PDF versions of each Mathematica code file, viewable by any users without Mathematica access.

### Data ('data')
This file contains (1) all output data from the experiment (both raw and in the formats needed to be read directly into each code file) and (2) all output data from simulation runs (you can recompute this data with the code provided, but this requires a significant amount of time and computational power). Included files are:
* 'autocorr_data.xlsx': Includes all experimental outputs in a readable format. 'Summary' provides an overview of all extinction experiment outcomes, 'rawdata' is the raw laboratory results (cell density counts), 'programmedtemps' is the experimental temperature time series programmed into incubators, 'templogging' is the thermal probe data observed from each experimental treatment, 'rawTPCdata' is the experimental thermal performance data gathered prior to the experiment, and 'rawTPCdata post' is the experimental thermal performance data gathered after the experiment.
* 'experimentalresults.csv': The extinction experiment outputs formatted to be read into the Mathematica code files.
* 'PcaudatumTPCdata.csv': The TPC experiment outputs formatted to be read into the Mathematica code files and the R TPC file. CHECK
* 'Rdata.csv': The extinction experiment outputs formatted to be read into the R stats file.
* 'SDE... .m': These files contain the outputs of the SDE model run for 100 replicates over 10,000 time steps under white ('gamma0'), pink ('gamma1'), and brown ('gamma2') noise. They are needed to recreate Figs 4a-c, S2, and S4.
* 'SSA2... .m': These files contain the outputs of the SSA model. Those with the extensions 'white', 'pink', and 'brown' were run for 40 replicates over 112 time steps (reflecting experimental conditions) and are needed to recreate Fig 6a-c; those with extensions 't1009 20reps' were run for longer time periods and are needed to recreate supplemental Fig S5.
* 'windowing... .m': These files contain the outputs of the r_min metric for each noise color (indicated by file extensions) and are needed to recreate Fig 4d.

## Operating Notes
Code was run in R v4.4.3 (open source; '.Rmd' files) and Wolfram Mathematica 14.1.0.0 ('.nb' files). To run code, download all files and update any 'directory' lines to reflect local data storage path; output files will automatically be stored in the same location.

## References
Lactin, D.J, N.J. Holliday, D.L. Johnson, and R. Craigen (1995). ["Improved Rate Model of Temperature-Dependent Development by Arthropods."](https://academic.oup.com/ee/article-abstract/24/1/68/2394752) Environmental Entomology 24(1): 68-75.

Padfield D., H. O’Sullivan, and F. Windram (2024). rTPC: Fitting and Analysing Thermal Performance Curves. R package version 1.0.7, [https://padpadpadpad.github.io/rTPC/](https://padpadpadpad.github.io/rTPC/), [https://github.com/padpadpadpad/rTPC](https://github.com/padpadpadpad/rTPC).

Robey, A.J., M.T. Kummel, and D.A. Vasseur (2025). ["Temporal autocorrelation increases temperature-driven extinction risk by clustering stressful conditions."](https://doi.org/10.1101/2025.07.29.667527) In review.

Robey, A.J. and D.A. Vasseur (2026). ["Order matters: Autocorrelation of temperature dictates extinction risk in populations with nonlinear thermal performance."](https://doi.org/10.1002/ecy.70325) Ecology 107(3): e70325. ([Code available here](https://github.com/arobey63/autocorrelation))

Vasseur, D.A., C. Bieg, M.T. Kummel, and A.J. Robey (2025). ["Forecasting Extinction Risk using Thermal Performance Curves and Population Dynamic Modeling."](https://doi.org/10.1101/2025.04.27.650737) In review. ([Code available here](https://github.com/dvasseur9/Forecasting-Extinction-Risk))
