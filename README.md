# Mutagenesis data

High-resolution neutral mutation rates analyzed in the paper [Probabilistic K-mean with local alignment for clustering and motif discovery in functional data](https://arxiv.org/abs/1808.04773), by Marzia A. Cremona and Francesca Chiaromonte. 

Mutation rates (substitutions, insertions and deletions) are estimated using the pipeline presented in [Kuruppumullage Don et al. (2013)](https://doi.org/10.1073/pnas.1221792110). 


## Raw data

#### `substitution_rates_hot_regions.txt`
Tab-separated file with the following columns:
- `chr`: chromosome name
- `start`: start position
- `end`: end position
- `region`: hot region number
- `window`: 1-kb window number
- `ARcoverage`: AR (Ancestral Repeats) subregion coverage
- `compared`: total number of compared nucleotides in the window
- `different`: number of different nucleotides in human and orangutan alignment
- `substitution`: estimated substitution rate

#### `insertion_and_deletion_rates_hot_regions.txt`
Tab-separated file with the following columns:
- `chr`: chromosome name
- `start`: start position
- `end`: end position
- `region`: hot region number
- `window`: 1-kb window number
- `ARcoverage`:AR (Ancestral Repeats) subregion coverage 
- `compared`: total number of compared nucleotides in the window
- `not_compared`: number of nucleotides not compared (1000 minus compared)
- `insertion`: estimated insertion rate
- `deletion`: estimated deletion rate


## Processed data

#### `substitution_rates.RData`
RData file containing three lists of length 43, with one element for each of the 43 hot regions considered:
- `substitution`: pre-processed substitution rate curves
- `substitution_smoothed`: smoothed substitution rate curves
- `substitution_smoothed_derivative`: smoothed substitution rate curve derivatives

#### `indel_rates.RData`
RData file containing three lists of length 43, with one element for each of the 43 hot regions considered:
- `indel`: pre-processed indel rate curves
- `indel_smoothed`: smoothed indel rate curves
- `indel_smoothed_derivative`: smoothed indel rate curve derivatives
