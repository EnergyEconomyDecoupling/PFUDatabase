
<!-- *********** -->

<!-- Note: README.md is generated from README.Rmd.   -->

<!-- Be sure to edit README.Rmd and generate the README.md file by Cmd/Ctl-shift-K -->

<!-- *********** -->

# PFU-Database

This repository contains analysis code for the fellowship project for
Paul Brockway. One goal of the fellowship is building a world database
of country-specific primary, final, and useful exergy for 1960–2015.

Analyses are completed using the
[drake](https://github.com/ropensci/drake) environment which provides
helpful dependency management. See the [drake
manual](https://books.ropensci.org/drake/) for details.

## Quick start

At the RStudio console, type

`library(drake)`  
`r_make()`

## Advanced

Consider setting RStudio keyboard shortcuts for executing the drake plan
in this repository. See `Tools|Modify keyboard shortcuts...`. Some
convenient keyboard shortcuts are:

  - `command-option-control-D` (for *d*rake) to execute the “Run a drake
    workflow” command on the `plan`
  - `command-option-control-V` (for *v*isualize) to execute “Visualize a
    drake workflow” command on the `plan`

With those keyboard shortcuts in place, the

`library(drake)`

command needs to be issued only *once* after first opening the project
in RStudio.

Thereafter, type the keyboard shortcut `command-option-control-D`
(instead of `r_make()`) to re-run the analysis. Type the keyboard
shortcut `command-option-control-V` (instead of `vis_drake_graph(plan)`)
to visualize the dependency tree as a directed acyclic graph. The
command `sankey_drake_graph(plan)` will produce a Sankey diagram of the
dependency tree.

## Contributors

  - Emmanuel Aramendia, University of Leeds
  - Paul Brockway, University of Leeds
  - Matthew Kuperus Heun, Calvin University
  - Zeke Marshall, University of Leeds
