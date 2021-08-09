# McH1-7 Probiotics_Trials

This project examines microbiome changes over time after application of the probiotic strain <i>Pseudoalteromonas</i> sp. McH1-7. Experimental setup: 4 colonies of <i>Montastraea cavernosa</i> (each a differnt genotype) were divided into at least 6 fragments and the fragments for each genotype were placed in the same aquarium (4 tanks total, one per genotype). Samples of the water and one of the coral fragments were saved just prior to probiotic application. Live culture of McH1-7 was added to the water and samples of the water were collected 1 hour after application. Water and coral fragments were then collected 1 day, 3 days, 7 days, 21 days, and 28 days after probiotic application. Water samples were filtered through a sterivex filter and DNA was extracted from the sterivex filter. Coral fragments were thawed, tissue/mucus was scrapped off, and DNA was extracted from the tissue/mucus. All water and tissue samples were analyzed for the presence of the korormicin gene from the probiotic strain <i>Pseudoalteromonas</i> sp. McH1-7. Additionally, all of the tissue samples were characterized by amplifying and sequencing the V4 region of the 16S rRNA gene. This repository contains all scripts and data for 1) the analysis of the korormicin ddPCR of water and tissue samples (KOR.R and kor_tank_long.txt) and 2) analysis of the 16S libraries from the tissue samples (remaining files). From this data, we would like to compare the detection of <i>Pseudoalteromonas</i> through ddPCR and 16S analysis. We are also interested in how the microbial community shifts (if at all) to application of the probiotic culture.

For the ddPCR, the mean number of gene copies and the standard error are calculated and then plotted with ggplot2 and ggforce to create a zoomed-in subplot. For the 16S amplicon libraries, sequencing files with all primers and illumina adaptors removed is available in this repository. First, dada2 is used to quality filter, join, and determine amplicon sequence variants. Chimeras are removed and taxonomy is assigned using the Silva v.138.1 formatted for dada2. Beta diversity is calculated with the Aitchison distance on center-log-transformed counts. A principal components analysis is performed with prcomp on the Aitchison distance and plotted with ggplot2. Phyloseq is used for creating stacked bar charts and the adonis package is used for PERMANOVA. All software versions are available in the session_info.txt file in this repository.
