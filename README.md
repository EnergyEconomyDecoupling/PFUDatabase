
<!-- *********** -->
<!-- Note: README.md is generated from README.Rmd.   -->
<!-- Be sure to edit README.Rmd and generate the README.md file by Cmd/Ctl-shift-K -->
<!-- *********** -->
<!-- badges: start -->

[![R-CMD-check](https://github.com/EnergyEconomyDecoupling/PFUDatabase/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/EnergyEconomyDecoupling/PFUDatabase/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->

# PFUDatabase [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5228375.svg)](https://doi.org/10.5281/zenodo.5228375)

This repository contains analysis code for the fellowship project of
Paul Brockway. One goal of the fellowship is building a world database
of country-specific primary, final, and useful exergy for 1960–2019.

Analyses are completed using the
[targets](https://github.com/ropensci/targets) environment which
provides helpful dependency management for the calculation pipeline.

This repository also includes a ShinyApp for visualization of the data
analyzed in the targets workflow.

## Quick start

At the RStudio console, type

``` r
library(targets)              # to load the targets package   
tar_visnetwork()              # to see a directed acyclic graph of the calculations that will take place   
tar_make_future(workers = 2)  # to execute the calculations (or `workers = 8`, if you have enough cores)
```

To run the App simply open the App.R script in the ShinyApp file and
click RunApp.

### Accessing targets

A list of targets can be found with `PFUDatabase::target_names`. A list
of target meanings can be found with `?PFUDatabase::target_names`.

`targets::tar_read(<<target>>)` pulls the value of a target out of the
`targets` cache. (`<<target>>` should be an unquoted symbol such as
`Specified`.)

### Fresh start

`targets::tar_destroy()` invalidates the `targets` cache and forces
reanalysis of everything. Reanalyzing everything may take a while.

### More Information

For information about the `targets` package, see the [targets
manual](https://books.ropensci.org/targets/).

For documentation on the `PFUDatabase` package, see
<https://EnergyEconomyDecoupling.github.io/PFUDatabase/>.

## Contributors

- Emmanuel Aramendia, University of Leeds
- Paul Brockway, University of Leeds
- Matthew Kuperus Heun, Calvin University
- Zeke Marshall, University of Leeds
