---
title: fem
weight: -11
---


<!-- <img src="man/figures/logo.png" align="right" alt="" width="220" /> -->

-   build:
    [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/fem)](http://cran.r-project.org/web/packages/fem)
    [![CRAN
    Downloads](http://cranlogs.r-pkg.org/badges/grand-total/fem?color=orange)](http://cran.r-project.org/package=fem)
    [![Package
    Status](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
    ![CRAN/METACRAN](https://img.shields.io/fem/l/fem?style=plastic)
-   github: [![Github
    Stars](https://img.shields.io/github/stars/atmoschem/fem.svg?style=social&label=Github)](https://github.com/atmoschem/fem)
    ![GitHub code size in
    bytes](https://img.shields.io/github/languages/code-size/atmoschem/fem)
    ![GitHub issues](https://img.shields.io/github/issues/atmoschem/fem)
    <!-- ![Liberapay giving](https://img.shields.io/liberapay/gives/sergio.ibarra) -->
    ![GitHub commit
    activity](https://img.shields.io/github/commit-activity/y/ibarraespinosa/fem)
    [![R build
    status](https://github.com/atmoschem/fem/workflows/R-CMD-check/badge.svg)](https://github.com/atmoschem/fem/actions)

<!-- ![](https://github.com/atmoschem/fem/raw/master/all_comp.gif) -->

# Fixed Emissions Model (FEM)

A model to speciate emissions. In the future, it will include estimation
methods, methods, classes and more.

It includes emissions from:

Kawashima, A. B., Martins, L. D., Abou Rafee, S. A., Rudke, A. P., \#’
de Morais, M. V., & Martins, J. A. (2020). \#’ Development of a
spatialized atmospheric emission inventory for the main \#’ industrial
sources in Brazil. Environmental Science and Pollution Research, 1-11.

## Installation

``` r
remotes::install_github("atmoschem/fem")
```

## Use

``` r
pm <- rnorm(n = 100, mean = 400, sd = 2)
(df <- fem::spec_industry(pm, code = "01_petroleum"))
#>                x                                   species
#>     1: 5.8170167 1-(1,1-dimethylethyl)-3,5-dimethylbenzene
#>     2: 5.7659381 1-(1,1-dimethylethyl)-3,5-dimethylbenzene
#>     3: 5.7898846 1-(1,1-dimethylethyl)-3,5-dimethylbenzene
#>     4: 5.8304557 1-(1,1-dimethylethyl)-3,5-dimethylbenzene
#>     5: 5.8368646 1-(1,1-dimethylethyl)-3,5-dimethylbenzene
#>    ---                                                    
#> 14496: 0.2073150                            vinyl chloride
#> 14497: 0.2063975                            vinyl chloride
#> 14498: 0.2068395                            vinyl chloride
#> 14499: 0.2065491                            vinyl chloride
#> 14500: 0.2069582                            vinyl chloride
```

Connection with [vein](https://github.com/atmoschem/vein)

FEM is designed to be used with VEIN and generate inputs for different
chemical mechanisms


