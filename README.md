# E.coli_ObgELPS
This repository contains scripts used for CRISPRi analyses of screens aimed at identifying an effect of ObgE on cell envelope/LPS synthesis

In short, the script uses DESeq2 to identify differentially enriched/depleted sgRNAs.
Next, to obtain results at the gene-level, the α Robust Rank Aggregation (α-RRA) method from the MAGeCK pipeline is applied in R.

Screening was done with E. coli MG1655 DaraBAD ileY::Ptet-dcas9 containing plasmid-encoded constitutively expressed sgRNAs (from Wang et al., doi: 10.1038/s41467-018-04899-x). In addition, cells contain either the pBAD33Gm (Vector control) or the pBAD33Gm-obgE (ObgE) plasmid.

Exponential phase screen:libraries were grown overnight in selective LB medium and diluted 100x into fresh medium in 2-fold. After 2 hours of growth, 100 ng/ml aTc (the inducer of dcas9 expression) was added to one of the duplicate culture tubes, while the CRISPRi system was not activated in the second duplicate. 30 min later, 0.2% arabinose was added to all tubes (both with and without aTc) to induce obgE expression. Cultures were grown for 6 hours before sampling. 

Stationary phase screen: libraries were grown overnight in selective LB medium and diluted 100x into fresh medium in 2-fold. After 8 hours of growth, 100 ng/ml aTc was added to one of the duplicate culture tubes and 0.2% arabinose was added to all tubes. Cultures were further incubated overnight for 16 hours. Next, cultures were diluted 100x into fresh selective LB medium with 0.2% arabinose but without aTc. After 8 hours of growth, cultures were sampled.
