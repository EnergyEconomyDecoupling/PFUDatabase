
<!-- *********** -->
<!-- Note: README.md is generated from README.Rmd.   -->
<!-- Be sure to edit README.Rmd and generate the README.md file by Cmd/Ctl-shift-K -->
<!-- *********** -->

# PFUDatabase [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5228375.svg)](https://doi.org/10.5281/zenodo.5228375)

This repository contains analysis code for the fellowship project for
Paul Brockway. One goal of the fellowship is building a world database
of country-specific primary, final, and useful exergy for 1960–2018.

Analyses are completed using the
[drake](https://github.com/ropensci/drake) environment which provides
helpful dependency management.

This repository also includes a ShinyApp for visualisation of the data
analysed in the drake workflow.

## Quick start

At the RStudio console, type

``` r
library(drake)           # to load the drake package   
source("_drake.R")       # to load the plan object
r_vis_drake_graph()      # to see a directed acyclic graph of the calculations that will take place   
r_make()                 # to execute the calculations
```

To run the App simply open the App.R script in the ShinyApp file and
click RunApp.

## Advanced

### Keyboard shortcuts

Consider setting RStudio keyboard shortcuts for executing the drake plan
in this repository. See `Tools|Modify keyboard shortcuts...`. Some
convenient keyboard shortcuts are:

-   `command-option-control-V` (for *v*isualize) to execute the
    “Visualize a drake workflow” command on the `plan`
-   `command-option-control-D` (for *d*rake) to execute the “Run a drake
    workflow” command on the `plan`

Type the keyboard shortcut `command-option-control-V` (instead of
`r_vis_drake_graph(plan)`) to visualize the dependency tree as a
directed acyclic graph. Type the keyboard shortcut
`command-option-control-D` (instead of `r_make()`) to re-run the
analysis.

### Accessing targets

A list of targets can be found with `PFUWorkflow::target_names`. A list
of target meanings can be found with `?PFUWorkflow::target_names`.

`drake::readd(<<target>>)` pulls the value of a target out of `drake`’s
cache. `<<target>>` should be a quoted character string such as
“Specified”.

`drake::loadd(<<target>>)` copies the value of a target out of `drake`’s
cache into the environment.

`PFUWorkflow::readd_by_country(<<target>>, <<country>>)` reads
country-specific data out of the `drake` cache. Both `<<target>>` and
`<<country>>` should be quoted strings. `<<country>>` should be a
3-letter ISO abbreviation such as “ESP” or “ZAF”. See
`?PFUWorkflow::readd_by_country` for more details.

### Fresh start

`drake::clean()` invalidates `drake`’s cache and forces reanalysis of
everything. Reanalyzing everything may take a while.

### More

See the [drake manual](https://books.ropensci.org/drake/).

## Contributors

-   Emmanuel Aramendia, University of Leeds
-   Paul Brockway, University of Leeds
-   Matthew Kuperus Heun, Calvin University
-   Zeke Marshall, University of Leeds
