# Functional DIvergence Pipeline

The GroupSim pipeline is used for identifying and filtering functional divergent (FD) sites in multiple sequence alignments (MSA).
The pipeline takes as input a MSA, two grouping files with the names of the species in the two groups, and the percentage of most divergent sites to filter out. 


GroupSim is used to score FD sites. It is written by Tony Capra (2008).

Reference: Capra JA and Singh M. (2008) Characterization and Prediction of
Residues Determining Protein Functional Specificity. Bioinformatics,
24(13): 1473-1480, 2008.

## Usage:

./gspipe -i {input} -p {output prefix}  -n {percentage} -f {first group} -s {second group}

for seperating the most (m) and least (l) divergent sites according to user specified percentages.


## Requirement:
R - version 4.x
Python - version 3.x

## Python Packages Needed:
Pandas, numpy, BioPython