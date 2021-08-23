gcookbook
================
DJR
23/08/2021

``` r
library(tidyverse)
library(gcookbook)
```

## 1.4 Loading a Delimited Text Data File (CSV)

When you want to load data from a delimited text file…

### `read.csv()`

## 1.5 Loading Data from an Excel File

`read_excel("datafile.xls", sheet=2)`

## 1.6 Loading Data from SPSS/SAS/Stata Files

``` r
library(foreign)
```

`read_sav("datafile.sav")` for SPSS file `read_sas()` for SAS
`read_dta()` for Stata

## 1.7 Chaining Functions Together with `%>%`, the Pipe Operator

You want to call one function, then pass the result to another function,
and another, in a way that is easily readable.

``` r
morley %>% 
  filter(Expt == 1) %>% 
  summary()
```

    ##       Expt        Run            Speed     
    ##  Min.   :1   Min.   : 1.00   Min.   : 650  
    ##  1st Qu.:1   1st Qu.: 5.75   1st Qu.: 850  
    ##  Median :1   Median :10.50   Median : 940  
    ##  Mean   :1   Mean   :10.50   Mean   : 909  
    ##  3rd Qu.:1   3rd Qu.:15.25   3rd Qu.: 980  
    ##  Max.   :1   Max.   :20.00   Max.   :1070
