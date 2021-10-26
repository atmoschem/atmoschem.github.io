---
title: 3. Configuración
weight: -9
geekdocCollapseSection: true
---

<!-- spellchecker-disable -->

{{< toc-tree >}}

<!-- spellchecker-enable -->


La configuración es una de las partes mas importantes del inventário. 
Aqui van los inputs necesarios y el orden de estos, 
permite que **vein** pueda estimar las emisiones usando sus funciones. 

Abajo aparece el bloque de scripts de configuración.



```r

# 0 Configuration
language <- "spanish" # spanish portuguese english
path <-  "config/inventory_ecuador.xlsx"
readxl::excel_sheets(path)

metadata <- readxl::read_xlsx(path = path, sheet = "metadata")
mileage <- readxl::read_xlsx(path = path, sheet = "mileage")
tfs <- readxl::read_xlsx(path = path, sheet = "tfs")
veh <- readxl::read_xlsx(path = path, sheet = "fleet_age")
fuel <- readxl::read_xlsx(path = path, sheet = "fuel")
fuel_spec <- readxl::read_xlsx(path = path, sheet = "fuel_spec")
pmonth <- readxl::read_xlsx(path = path, sheet = "fuel_month")
met <- readxl::read_xlsx(path = path, sheet = "met")
euro <- readxl::read_xlsx(path = path, sheet = "euro")
tech <- readxl::read_xlsx(path = path, sheet = "tech")
year <- 2019
month <- 6
agemax <- 40
provincia <- unique(fuel$region)[1]
# provincia <- unique(fuel$region)[as.numeric(basename(getwd()))]
col_region <- "region" # esta columna debe estar presente en fuel y met
scale <- "none"
theme <- "black" # dark clean ing
delete_directories <- TRUE
source("config/config.R", encoding = "UTF-8")
```

El script `config.R` lee la información, procesa los data.frames y luego
genera los plots de todos los datos. 
Los gráficos son guardados en la carpeta images.
De esta forma es facil ver algun problema con los datos. 

