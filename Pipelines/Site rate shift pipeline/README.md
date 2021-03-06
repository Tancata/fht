# Site Rate Shift 

The Site Rate Shift pipeline is used for identifying and filtering sites that have experienced changes in evolutionary rates.
The pipeline takes as input a MSA, two rate files with the evolutionary rates of sites in two groups of organisms, and the percentage of sites to filter out. 

## Usage:

./srpipe -f {firstrate} -s {secondrate} -o {rateoutput} -p {percentage} -a {alignment} -u {finalouput}

All options must be specified.

## Input:
The rate files can be prepared by running iqtree on two groups of organisms on the same sites with `--rate` options to infer the site-specific rates. For details, take a look at Section **Inferring Site-Specific Rate** on http://www.iqtree.org/doc/Advanced-Tutorial 

Options | Details 
--------|--------
 firstrate  | Site-specific rate for first group of organisms
 secondrate | Site-specific rate for second group of organisms
 rateoutput | The name of the rate comparison file
 percentage | The percentage of sites to filter
 alignment | The original multiple sequence alignment in phylip format
 finaloutput | The filename for the finaloutput alignment file

#### Output
The two key output files are `{finaloutput}_rs_top{percentage}.phy` and `{finaloutput}_rs_bottom{percentage}.phy`, which contains the sites that have experienced the most and least amount of rate shifts. 

If the input for {percentage} is 40, then 40% of the sites will end up in `{finaloutput}_rs_bottom{percentage}.phy`, and 60% in `{finaloutput}_rs_top{percentage}.phy`. 

## Requirement:
1. R - version 4.x
2. Python - version 3.x

## Python Packages Needed:
Pandas, numpy, BioPython

## R packages Needed:
vroom, stringr, tidyverse
