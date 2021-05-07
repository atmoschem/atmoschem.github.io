---
title: emep
weight: -14
---

# EMEP EEA Emission factors data-base

Access to the EMEP EEA emission factors tier 2.
<https://www.eea.europa.eu/publications/emep-eea-guidebook-2019>

### Installation

``` r
library(remotes) 
install_gitlab("ibarraespinosa/emep")
```

## Functions

  - ef
  - find\_ef

<!-- end list -->

``` r
ef()
```

``` r
find_ef("electricity")
       NFR                                 Sector      Table                   Type                                   Technology        Fuel Abatement Region Pollutant Value  Unit
2  1.A.1.a Public electricity and heat production Table_3-20 Tier 2 emission factor Stationary reciprocating Engines - gas-fired Natural gas             <NA>        Cr  0.05 mg/GJ
11 1.A.1.a Public electricity and heat production Table_3-20 Tier 2 emission factor Stationary reciprocating Engines - gas-fired Natural gas             <NA>       TSP     2  g/GJ
   CI_lower CI_upper            Reference
2      0.01     0.25 Nielsen et al., 2010
11     1.00     3.00          BUWAL, 2001
```

