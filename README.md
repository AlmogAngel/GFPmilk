# GFP+ Maternal Cells in Puppy Blood: Single-Cell RNA-seq Analysis

This repository contains the analysis code and documentation for our study investigating GFP+ maternal cells detected in puppy blood samples.

## Overview

This project analyzes single-cell RNA-seq data from mouse blood samples comparing GFP+ experimental conditions to control samples. The analysis identifies and characterizes maternal cells that cross the placental barrier and persist in offspring circulation.

## Repository Contents

- **`make_figures.qmd`**: Main analysis workflow in Quarto format
  - Quality control and filtering
  - Cell type annotation
  - Differential expression analysis
  - Pathway enrichment analysis
  - Publication-quality figure generation

## Key Findings

- Detection of GFP+ maternal cells in puppy blood samples
- Characterization of macrophage populations
- Differential gene expression and pathway analysis between GFP+ and control samples

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
