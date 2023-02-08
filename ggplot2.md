ggplot2
================
Jason
2023-02-08

## Setting up my environment

Notes : setting up by loading `tidyverse` and `palmerpenguins` packages

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.4.0     ✔ purrr   1.0.1
    ## ✔ tibble  3.1.8     ✔ dplyr   1.1.0
    ## ✔ tidyr   1.3.0     ✔ stringr 1.5.0
    ## ✔ readr   2.1.3     ✔ forcats 1.0.0
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
library(palmerpenguins)
```

## FACET

``` r
ggplot(data = penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y = body_mass_g,color=species))+
  facet_wrap(~species)
```

    ## Warning: Removed 2 rows containing missing values (`geom_point()`).

![](ggplot2_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->
