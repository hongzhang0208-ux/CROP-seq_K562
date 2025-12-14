# CROP-seq-K562
Analysis code for CROP-seq CRISPRi experiments in K562 cells targeting transcription factors and reconstructing gene regulatory networks.

## Overview
This repository contains code for analyzing CROP-seq CRISPRi datasets in K562 cells.
The analysis focuses on quality control, knockdown cell identification and gene regulatory network (GRN) reconstruction.

## Data Availability
This repository does not contain raw or processed single-cell sequencing data.
To run the analysis, users need to provide:
- CellRanger output files (e.g. `filtered_feature_bc_matrix.h5`)
- sgRNA assignment files (e.g. sgRNA calls per cell)
- gRNA file: An example have beed uploaded (gRNA.xlsx)
  
Due to data size and data sharing policies, the sequencing data are not included in this repository.

## Analysis
The pipeline includes:
- sgRNA assignment
- Quality control
- Mixscape to identify KD cells
- Differential expression analysis
- Gene regulatory network inference

## Repository Structure

- `analysis/`: R Markdown files for Mixscape and SCENIC analysis
- `data/`: Input annotation files (e.g. sgRNA-to-gene mapping)
- `env/`: R session information for reproducibility

## Requirements
R with Seurat package for normal single-cell RNA-seq analysis and SCENIC package for GRNs inference.
