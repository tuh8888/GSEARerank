# GSEA Rerank

Harrison Pielke-Lombardo, Rani Powers, Aik Choon Tan, James Costello

University of Colorado Anschutz Medical Campus

### R Scripts

#### R/00-queryGEO.R

Queries GEO for all human gene expression studies that have .CEL files available. Saves a table of the studies and their descriptions to `RData/full_human_expression_GEO.rds`.

#### R/01-annotateStudies.R

Filters the big table of studies for those using Affymetrix Human Genome U133 Plus 2.0 Array with at least n = 6 samples. Annotate the studies for those that contain 'vehicle,' 'drug', 'treatment,' etc in the titles or descriptions. Write out table as a text file for manual annotation of control vs drug-treated samples.

### Java Code

#### edu/mit/broad/genome/alg/gsea

KSTests.java: Kolmogorov-Smirnov Enrichment Test related methods
KSCore.java: This is the core class that implements the Kolmogorov-Smirnov algorithm
PValueCaculatorImpls.java: The GSEA style implementation of pvalues and FDRs and FWERs

#### edu/mit/broad/genome/alg/fdr/FdrAlgs.java

False discovery rate algorithms.

#### edu/mit/broad/genome/alg/markers

AbstractPermutationTest.java
PermutationTest.java
PermutationTestBuilder.java





