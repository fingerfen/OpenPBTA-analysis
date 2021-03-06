# Gene Set Enrichment Analysis

Written by Stephanie J. Spielman to supercede previous analyses in [`ssgsea-hallmark`](https://github.com/AlexsLemonade/OpenPBTA-analysis/tree/master/analyses/ssgsea-hallmark). Primary goals include:

1. Score hallmark pathways based on expression data using GSVA analysis, using a strategy that produces Gaussian-distributed scores.
2. Analyze scores for highly significant differences among tumor classifications 


## Folder Content

+ `01-conduct-gsea-analysis.R` performs the GSVA analysis using RSEM FPKM expression data for both stranded and polyA data. Results are saved in `results/` TSV files.

+ `02-gsea-explore.Rmd` performs some initial exploratory analyses on GSVA scores including modeling and visualization.

+ `results/gsva_scores_stranded.tsv` represents GSVA scores calculated from `pbta-gene-expression-rsem-fpkm-collapsed.stranded.rds` (data release v12)
	+ File created with: `Rscript --vanilla 01-conduct-gsea-analysis.R --input pbta-gene-expression-rsem-fpkm-collapsed.stranded.rds --output gsva_scores_stranded.tsv`
+ `results/gsva_scores_polya.tsv` represents GSVA scores calculated from `pbta-gene-expression-rsem-fpkm-collapsed.polya.rds` (data release v12)
	+ File created with: `Rscript --vanilla 01-conduct-gsea-analysis.R --input pbta-gene-expression-rsem-fpkm-collapsed.polya.rds --output gsva_scores_stranded.tsv`