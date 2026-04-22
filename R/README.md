# Code and Data for: *Are handwritten letter forms shaped by morphology?*

This repository contains the code and data necessary to reproduce the statistical analyses presented in the paper:

**Petitjean, S., Berg, K., Wieler, J., Huber, H., & Hartmann, S.**  
*Are handwritten letter forms shaped by morphology?*

## Overview

The repository provides the data and scripts used for modeling pen trajectories using Generalized Additive Models (GAMs). It represents a subset of the full processing pipeline, focusing on the final stages of the analysis (i.e., model fitting and evaluation).

## Repository structure

- `trajectories/`  
  Contains the extracted pen trajectories. Each file corresponds to a single trajectory.

- `trajectories/features.csv`  
  A table containing linguistic and non-linguistic features associated with each trajectory (e.g., morphological category, positional information, and other predictors used in the models).

- `filtered_filenames/`  
  Contains lists of trajectory filenames that were manually validated and retained for analysis.

- `gam.R` (main script)  
  The R script used to fit the models and generate the results reported in the paper.

## Usage

The analysis can be run using R. The main script is designed to be executed from the command line:

```bash
Rscript main_script.R

## Requirements

The code requires R (≥ 4.0 recommended) and the following CRAN packages:

- mgcv
- itsadug
- ggplot2
- scales

All packages can be installed directly from CRAN, e.g.:

```r
install.packages(c("mgcv", "itsadug", "ggplot2", "scales"))