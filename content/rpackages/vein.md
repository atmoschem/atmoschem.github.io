---
title: vein
weight: -19
---

<img src="https://raw.githubusercontent.com/atmoschem/vein/master/man/figures/logo.png" align="right" alt="" width="220" />

-   build: [![Travis-CI Build
    Status](https://travis-ci.org/atmoschem/vein.svg?branch=master)](https://travis-ci.org/atmoschem/vein)
    [![AppVeyor Build
    Status](https://ci.appveyor.com/api/projects/status/github/ibarraespinosa/vein?branch=master&svg=true)](https://ci.appveyor.com/project/ibarraespinosa/vein)
    [![Coverage
    Status](https://img.shields.io/codecov/c/github/atmoschem/vein/master.svg)](https://codecov.io/github/atmoschem/vein?branch=master)
-   cran:
    [![](http://cranlogs.r-pkg.org/badges/vein)](http://cran.rstudio.com/web/packages/vein/index.html)
    [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/vein)](http://cran.r-project.org/web/packages/vein)
    [![CRAN
    Downloads](http://cranlogs.r-pkg.org/badges/grand-total/vein?color=orange)](http://cran.r-project.org/package=vein)
    [![Package
    Status](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
    ![CRAN/METACRAN](https://img.shields.io/cran/l/vein?style=plastic)
-   doi:
    [![DOI](https://zenodo.org/badge/88201850.svg)](https://zenodo.org/badge/latestdoi/88201850)
-   github: [![Github
    Stars](https://img.shields.io/github/stars/atmoschem/vein.svg?style=social&label=Github)](https://github.com/atmoschem/vein)
    ![GitHub code size in
    bytes](https://img.shields.io/github/languages/code-size/atmoschem/vein)
    ![GitHub
    issues](https://img.shields.io/github/issues/atmoschem/vein)
    <!-- ![Liberapay giving](https://img.shields.io/liberapay/gives/sergio.ibarra) -->
    ![GitHub commit
    activity](https://img.shields.io/github/commit-activity/y/ibarraespinosa/vein)
    [![R build
    status](https://github.com/atmoschem/vein/workflows/R-CMD-check/badge.svg)](https://github.com/atmoschem/vein/actions)

<!-- ![](https://github.com/atmoschem/vein/raw/master/all_comp.gif) -->

# **V**ehicular **E**missions **IN**ventories (VEIN)

![](https://i.imgur.com/stnHJQx.png)

### What is new?

-   *Added OpenMP AGAIN and also, imported dotCall64 to avoid copying*
-   New VEIN project: sebr\_cb05co2 covers SP, MG, RJ with CB05+CO2 for
    2019 and amazon2014.
-   NH3 in ef\_cetesb
-   updated VOC speciation for Brazil

## New in VEIN?

No worries! Just install
[R](https://www.google.com/search?q=install+R&oq=install+R&aqs=chrome..69i57j35i39l2j0l3j69i60l2.1308j0j7&sourceid=chrome&ie=UTF-8),
[Rstudio](https://www.google.com/search?sxsrf=ALeKk00EtkaL-W834eJbAfWxSgAtHlzAuw%3A1600952042358&ei=6pZsX7G5FaS65OUP9NuOqAk&q=install+Rstudio&oq=install+Rstudio&gs_lcp=CgZwc3ktYWIQAzIFCAAQywEyBQgAEMsBMgUIABDLATIFCAAQywEyBQgAEMsBMgUIABDLATIFCAAQywEyBQgAEMsBMgUIABDLATIFCAAQywE6BAgAEEdQiaIBWJSoAWCPqgFoAHABeAGAAaMCiAGuB5IBBTAuNS4xmAEAoAEBqgEHZ3dzLXdpesgBCMABAQ&sclient=psy-ab&ved=0ahUKEwix1qWO64HsAhUkHbkGHfStA5UQ4dUDCA0&uact=5)
and then

### System requirements

vein imports functions from spatial packages listed below. In order to
install these packages, firstly the user must install the requirements
mentioned [here](https://www.github.com/r-spatial/sf).

### Installation

VEIN can be installed via CRAN or github

``` r
install.packages("vein")
```

gitlab (faster than github)

``` r
remotes::install_gitlab("ibarraespinosa/vein")
```

github

``` r
remotes::install_github("atmoschem/vein")
```

### 1. get a project (easier)

At the moment, most of the projects covers Brazilian regions, but I will
include China, Europe or USA approaches as soon as I can.

Use the function
[get\_project](https://atmoschem.github.io/vein/reference/get_project.html)
and read the documentation.

-   [![R build
    status](https://github.com/atmoschem/vein/workflows/brazil_bu/badge.svg)](https://github.com/atmoschem/vein/actions)
-   [![R build
    status](https://github.com/atmoschem/vein/workflows/brazil_bu_csvgz/badge.svg)](https://github.com/atmoschem/vein/actions)
-   [![R build
    status](https://github.com/atmoschem/vein/workflows/brazil_bu_csv/badge.svg)](https://github.com/atmoschem/vein/actions)
-   [![R build
    status](https://github.com/atmoschem/vein/workflows/brazil_td_chem/badge.svg)](https://github.com/atmoschem/vein/actions)
-   [![R build
    status](https://github.com/atmoschem/vein/workflows/brazil_bu_chem/badge.svg)](https://github.com/atmoschem/vein/actions)
-   [![R build
    status](https://github.com/atmoschem/vein/workflows/sebr_cb05co2/badge.svg)](https://github.com/atmoschem/vein/actions)
-   [![R build
    status](https://github.com/atmoschem/vein/workflows/amazon2014/badge.svg)](https://github.com/atmoschem/vein/actions)

``` r
library(vein)
?get_project
get_project(directory = "awesome_city")
```

The structure of the new directory “awesome\_city” is:

``` r
awesome_city
├── config
│   ├── clean.R
│   ├── config.R
│   ├── inventory.xlsx
│   └── packages.R
├── main.R
├── main.Rproj
├── network
│   ├── net.gpkg
│   └── net.rds
├── scripts
│   ├── evaporatives.R
│   ├── exhaust.R
│   ├── fuel_eval.R
│   ├── net.R
│   ├── pavedroads.R
│   ├── plots.R
│   ├── post.R
│   ├── traffic.R
│   └── wrf.R
└── wrf
└── wrfinput_d02
```

You have to open the file `main.Rproj` with Rstudio and then open and
run `main.R`

To run `main.R` you will need these extra packages:

-   ggplot2
-   readxl
-   eixport (If you plan to generate WRF Chem emissions file)

If you do not have them already, you can install:

``` r
install.packages(c("ggplot2", "readxl", "eixport"))
```

## Too complicated? Watch a YouTube

<iframe width="560" height="315" src="https://www.youtube.com/embed/tHSWIjg26vg" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>

[English](https://www.youtube.com/embed/tHSWIjg26vg)

<iframe width="560" height="315" src="https://www.youtube.com/embed/6-07Y0Eimng" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>

[Portuguese](https://www.youtube.com/watch?v=6-07Y0Eimng)

