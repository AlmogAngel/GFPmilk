# Maternal Cell Transfer via Milk: Single-Cell RNA-seq Analysis

This repository contains the analysis code and documentation for single-cell RNA-seq analysis of maternal cells transferred through milk to nursing pups.

## Overview

This project analyzes single-cell RNA-seq data from mouse pup blood samples to identify and characterize maternal cells transferred via nursing. Using GFP-labeled maternal cells, we track and analyze transferred immune cells in the offspring circulation, focusing on macrophage populations and their transcriptional signatures.

## Repository Contents

- **`make_figures.qmd`**: Main analysis workflow in Quarto format
  - Quality control and filtering
  - Cell type annotation
  - Differential expression analysis
  - Pathway enrichment analysis
  - Publication-quality figure generation

## Key Findings

- Identification of maternal cells transferred via milk in nursing pup blood
- Characterization of transferred macrophage populations  
- Differential gene expression and pathway analysis of maternal vs. control cells
- Evidence of maternal immune cell transfer through lactation

## Analysis Workflow

1. **Data Loading**: Process 10X Genomics single-cell data
2. **Quality Control**: Filter cells based on QC metrics
3. **Doublet Detection**: Remove doublets using scDblFinder
4. **Normalization**: Log-normalize and scale data
5. **Dimensionality Reduction**: PCA and UMAP
6. **Cell Type Annotation**: Manual and automated (SingleR) annotation
7. **Differential Expression**: Compare GFP+ vs control macrophages
8. **Pathway Analysis**: Enrichment analysis using MSigDB gene sets

## Requirements

### R Packages
- Seurat
- SingleR
- tidyverse
- dittoSeq
- ggrepel
- scDblFinder
- mascarade
- msigdbr
- UCell
- patchwork

## Usage

To reproduce the analysis:

```r
# Open and render the Quarto document
quarto::quarto_render("make_figures.qmd")
```

## Output

The analysis generates publication-ready figures including:
- UMAP visualizations by sample origin and cell type
- Volcano plots for differential expression
- Pathway enrichment heatmaps
- Dotplots for marker gene expression

## Contact

For questions about this analysis, please open an issue in this repository.

## License

This project is licensed under the MIT License.
