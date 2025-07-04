# Data_-_Codes_2025
This repository contains all the data and code required to replicate the models, calculations, and figure generation described in the paper by Vidal-Cordasco, Rodríguez-Gómez, and Marín-Arroyo (submitted). The entire workflow can be reproduced using R (tested with version 4.5.0 in RStudio) and NetLogo (version 6.4).

To successfully replicate the analyses, the scripts and resources in this repository should be executed in the following order:

1) Species_Distribution_Models Folder
This folder contains a subfolder named Bilinear_interpolated_variables, which includes all paleoclimate and environmental variables derived from the HadleyCM3 model (Krapp et al. 2021), interpolated to a 0.25º spatial resolution. The Data.xlsx file compiles all MIS 3 faunal occurrence records used in the Species Distribution Models (SDMs).

The script SpeciesDistributionModels.R builds, evaluates, and projects habitat favorability models for each primary and secondary consumer species. The resulting outputs are stored in the Carrying_Capacity folder for further use.

2) Carrying_Capacity Folder
This folder includes 45 subfolders, each corresponding to a species included in the study. Each subfolder contains the species' SDM and associated habitat favorability outputs.

Four additional .xlsx files are included:

Prey_preferences.xlsx – Contains body mass, energy requirements, and predation percentages for each secondary consumer over various prey sizes. These are provided under four human meat intake scenarios (30%, 40%, 50%, and 60%), each in a separate sheet.

PopStructure.xlsx – Details life history traits and age-specific body mass estimates for each primary consumer, based on Gompertz growth curves. These data inform Weibull models used to reconstruct population structures.

MNI_Comparison.xlsx – Provides maximum estimated population densities for each species at MIS3 archaeological sites where minimum numbers of individuals (MNI) are reported.

Carrying_Capacity.R – This script estimates the carrying capacity of secondary consumers, including humans. Output files generated by this script are stored in the Herbivore_Biomass_Outputs folder.

3) Near_model Folder
This folder contains the NetLogo implementation of the NEAR agent-based model, along with its required input data and analysis tools.

The data subfolder includes human carrying capacity estimates under different meat intake assumptions (previously generated in the DIET folder within Herbivore_Biomass_Outputs) and an elevation map of Europe.

The Outputs folder contains simulation outputs from various NEAR experiments.

The NEAR_Analyses.R script performs all statistical analyses and reproduces the figures presented in the manuscript.



If you encounter any issues or have questions about running the code, please contact: marcovidalcordasco@gmail.com

