01\_write-installed-packages.R
================
kyrene
Tue Jan 15 17:19:15 2019

``` r
## deja vu from earlier!

library(tidyverse)
```

    ## ── Attaching packages ───────────────────────────────────────────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 3.1.0     ✔ purrr   0.2.5
    ## ✔ tibble  2.0.1     ✔ dplyr   0.7.8
    ## ✔ tidyr   0.8.2     ✔ stringr 1.3.1
    ## ✔ readr   1.3.1     ✔ forcats 0.3.0

    ## ── Conflicts ──────────────────────────────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
## create a data frame of your installed packages
## hint: installed.packages() is the function you need
ipkgs <- installed.packages() %>% as_tibble()

ipkgs <- ipkgs %>%
  select(
    Package,
    LibPath,
    Version,
    Priority,
    Built
  )
## optional: select just some of the variables, such as
##   * Package
##   * LibPath
##   * Version
##   * Priority
##   * Built

## write this data frame to data/installed-packages.csv
## hint: readr::write_csv() or write.table()
## idea: try using here::here() to create the file path

library(here)
```

    ## here() starts at /Users/kyrene/Desktop/rstudio-conf2019/packages-report

``` r
here::here('data','installed-packages.csv')
```

    ## [1] "/Users/kyrene/Desktop/rstudio-conf2019/packages-report/data/installed-packages.csv"

``` r
## YES overwrite the file that is there now (or delete it first)
## that's a old result from me (Jenny)
## it an example of what yours should look like and where it should go
```
