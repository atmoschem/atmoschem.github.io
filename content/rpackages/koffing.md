---
title: koffing
weight: -15
author: William Amorim
---

<img src="man/figures/logo.png" align="right" width = "15%">

The goal of `koffing` is to assemble R functions to catch (scrape) air
pollution data. `koffing` is from the same creator of the blog
[Rpollution](https://rpollution.com). Newer versions of this scraper can
be found [here](https://github.com/williamorim/rpollution).

## Installation

You can install `koffing` from github with:

``` r
# install.packages("devtools")
devtools::install_github("atmoschem/koffing")
```

## CETESB scraper

To scrape data from the CETESB qualar system, use the function
`scraper_cetesb()`.

``` r
library(koffing)

koffing::scraper_cetesb(
  parameter = 99, 
  station = 17, 
  start = "01/01/2018", 
  end = "31/01/2018", 
  login = "login", 
  password = "password"
)
```

If you substitute the values `login` and `password` by your login and
password from the Qualar system, this example will return the hourly NO
concentrations from the Pinheiros station for January 2018.

