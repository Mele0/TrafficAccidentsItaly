---
title: "Spatio-temporal analysis of traffic accident injuries in Italy (2017–2022)"
output:
  github_document:
    toc: true
    df_print: tibble
---

<!-- badges: start -->
<!-- You can add badges later, e.g., R version, license, DOI -->
<!-- badges: end -->

## Overview

This repository contains the analysis and report for a provincial-level spatio-temporal study of road-traffic accident (RTA) injuries across Italy from 2017 to 2022. The work uses Bayesian hierarchical Poisson log-linear models with BYM2 spatial effects and random-walk temporal components to estimate relative risks and assess temperature and social vulnerability as covariates. See the full PDF in `reports/HDA_Group7.pdf`.  

## What’s inside

- `HDA_Group7.Rmd` is the main analysis notebook.  
- `reports/HDA_Group7.pdf` is the final report.  
- `figs/` holds maps and figures generated when knitting.  
- `data/` contains data guidance and (optionally) small samples.  
- `scripts/` is for helper code (e.g., data prep or download).  

## Quick start

Install packages and render the notebook. The project uses `renv` to lock dependencies.

```r
install.packages("renv")
renv::init()
# Add the packages you use, for example:
pkgs <- c("tidyverse","sf","spdep","INLA","Matrix","tmap","ggplot2","lubridate","janitor","patchwork","knitr","rmarkdown")
install.packages(setdiff(pkgs, rownames(installed.packages())))
renv::snapshot()
