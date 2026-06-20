# TCGA-LUAD DNA Methylation Analysis

## Overview
Differential methylation analysis of lung adenocarcinoma (LUAD) using TCGA 450k array data.

## Dataset
- **Source:** TCGA-LUAD via GDC portal
- **Platform:** Illumina Human Methylation 450k
- **Samples:** 50 Primary Tumor + 32 Normal tissue
- **CpG sites:** 485,577 → 396,164 after filtering

## Methods
1. **Data retrieval** — TCGAbiolinks + SeSAMe normalization
2. **Filtering** — Removed sex chromosomes + high NA CpGs
3. **Differential methylation** — limma linear model
4. **Visualization** — Volcano plot + heatmap

## Key Results
- 15,578 hypermethylated CpGs in tumor (padj < 0.05, ΔBeta > 0.2)
- 7,314 hypomethylated CpGs in tumor
- Top 50 CpGs perfectly separate tumor from normal tissue

## Outputs
| File | Description |
|------|-------------|
| volcano_methylation.png | Differential methylation volcano plot |
| methylation_heatmap.png | Top 50 DM CpGs heatmap |

## Tools
R, TCGAbiolinks, minfi, limma, sesame, pheatmap, ggplot2

## Author
Lokaveenasri — Biotechnology B.Tech, Rajalakshmi Engineering College

