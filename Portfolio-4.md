Portfolio 4: Demographic and Pre-Screen Info
================

As per journal guidelines, I had to report demographic information for
my submission. Additionally, I reported some brief descriptive
information on the major life events experienced by my sample, which was
pertinent to the research question. For this portfolio piece, I will be
recreating these pre-liminary analyses with my newly minted .rds files.

``` r
library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.5.2     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.4     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.4     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
library(readr)
library(janitor)
```

    ## 
    ## Attaching package: 'janitor'
    ## 
    ## The following objects are masked from 'package:stats':
    ## 
    ##     chisq.test, fisher.test

``` r
demographic_data <- readRDS("demographic_data.rds")
life_event_data <- readRDS("life_event_data.rds")
```

## Including Plots

You can also embed plots, for example:

``` r
demographic_data <- demographic_data %>% clean_names()

names(demographic_data)
```

    ##  [1] "pid"                  "age"                  "sex"                 
    ##  [4] "ethnicity_simplified" "student_status"       "employment_status"   
    ##  [7] "x7"                   "x8"                   "x9"                  
    ## [10] "x10"                  "x11"                  "x12"                 
    ## [13] "x13"

``` r
#had to clean these variables out
demographic_data <- demographic_data %>%
  select(-x7, -x8, -x9, -x10, -x11, -x12, -x13)
```

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
