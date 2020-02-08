# TAS
This repository contains the source code and data to regenerate the transformation activity scores using ordered logistic regression model with random effects from our paper about FGFR variants.

# Supplementary Code
> I. Takeda-Nakamura et al., "Title TBD", in submission. 

## Contents

- [Overview](#overview)
- [System Requirements](#system-requirements)
- [Instructions for Use](#instructions-for-use)

# Overview

We developed an ordered logistic regression model with random effects for evakuating analyzing the the transformation activity of FGFR variants. We performed four experimental batches of the focus formation assay and also four experimental batches of the low-serum cell proliferation assay. All the experimental results of both assays were scored in four classes. Due to differences in culture conditions, batch-to-batch variations in the obtained scores were observed. We defined transformation activity scores (TASs) by integrating all the experimental results and set for four classes commensurate with the scores of each assay. To calculate TASs with batch-to-batch adjustment, we utilized the ordered logistic regression model with random effects.

# System Requirements

## Hardware Requirements

The scripts requires only a standard computer with enough RAM to support the operations defined by a user. For minimal performance, this will be a computer with about 8 GB of RAM. For optimal performance, we recommend a computer with the following specs:

RAM: 32+ GB  
CPU: 4+ cores, 4.0+ GHz/core

The runtimes below are generated using a computer with the recommended specs (32 GB RAM, 4 cores@4.2 GHz) and internet of speed 100 Mbps.

## Software Requirements

### `R` and Rstan

This script files runs on `R` and Rstan for Windows, Mac, or Linux, which requires the R version 3.4.0 or later. For install instructions, visit the RStan Getting Started website at
https://github.com/stan-dev/rstan/wiki/RStan-Getting-Started 


### Package dependencies

Users should install the following packages prior to use the scripts, from an `R` terminal:

```
install.packages(c('reshape2', 'rstan', 'tidyverse', 'shinystan'))
```

which will install in about 5 minutes on a recommended machine.

### Package Versions

This  with all packages in their latest versions as they appear on `CRAN` on April 13, 2019. Users can check [CRAN snapshot](https://mran.microsoft.com/timemachine/) for details. The versions of software are, specifically:

```
"rstan version: 2.18.2"
"tidyverse version: 1.2.1"
"reshape2 version: 1.4.3"
"shinystan version: 2.5.0"
```

If you are having an issue that you believe to be tied to software versioning issues, please drop us an [Issue](https://github.com/neurodata/mgc/issues). 

# Instructions for Use

Please put all the files in the same directory, and set the working directory appropriately.

# Reproducibility

All the code and data are available in TAS.Rmd and Data.csv to reproduce TASs in our paper. Each Bayesian inference takes about 10-20 minutes on a recommended machine.

Inference results will be saved as FGFR-FFA_score.tsv.

TAS.pdf generated from TAS.Rmd includes all scripts with information.

```
├── README.md
├── TAS.Rmd
├── Dada.csv
└── FGFR-FFA_score.tsv

0 directories, 4 files
```
