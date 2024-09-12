---
title: "Proyecto Final Diplomado"
author: "Edouard Acuña Kohnenkamp"
format: 
   html:
     toc: true
     code-fold: show
---

::: {.cell}

```{.r .cell-code}
#/ label: setup
#/ include: false

knitr::opts_chunk$set(
  echo = TRUE,
  warning = FALSE,
  message = FALSE,
  fig.width = 7,
  fig.height = 5,
  fig.align = "center"
)
```
:::




## Carga de librerías

Librerias necesarias para proyecto final



::: {.cell layout-align="center"}

```{.r .cell-code}
library(tidyverse)
library(readxl)
```
:::



## Carga de base de datos

Base de datos en formato excel



::: {.cell layout-align="center"}

```{.r .cell-code}
DATA_RESUMEN <- read_excel("bases/DATA_RESUMEN.xlsx")
View(DATA_RESUMEN)
```
:::



## Procesamiento de datos



::: {.cell layout-align="center"}

```{.r .cell-code}
DATA_RESUMEN <- DATA_RESUMEN %>% 
                mutate(SUELO = as.factor(SUELO),
                       TRATAMIENTO = as.factor(TRATAMIENTO),
                       REPETICION = as.factor(REPETICION))
```
:::

