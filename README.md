# scRNA-seq Multi-sample Processing and CellPhoneDB Preparation Pipeline

This repository contains a simple workflow for processing multi-sample single-cell RNA-seq data, including sample integration, basic preprocessing, automatic cell type annotation with CellTypist, preparation of CellPhoneDB input files, and running CellPhoneDB for cell–cell communication analysis.

## Workflow Overview

The pipeline includes the following main steps:

1. **Multi-sample integration**
   - Load single-cell expression data from multiple samples.
   - Merge samples into one unified object.
   - Preserve sample-level metadata for downstream comparison.

2. **Basic preprocessing**
   - Quality control of cells and genes.
   - Filtering of low-quality cells.
   - Normalisation of expression data.
   - Identification of highly variable genes.
   - Dimensionality reduction.
   - Clustering and visualization.

3. **Cell type annotation using CellTypist**
   - Use CellTypist to automatically predict cell types.
   - Add predicted cell type labels to the metadata.
   - Optionally compare predicted labels with clustering results.
   - Generate annotated UMAP/tSNE plots.

4. **Preparation of CellPhoneDB input files**
   - Extract the processed expression matrix.
   - Prepare the cell metadata file required by CellPhoneDB.
   - Ensure that cell barcodes and cell type labels are correctly matched.
   - Format input files according to CellPhoneDB requirements.

5. **CellPhoneDB analysis**
   - Run CellPhoneDB statistical analysis.
   - Identify potential ligand–receptor interactions between annotated cell types.
   - Generate interaction result tables for downstream interpretation.

## Expected Input

The workflow is designed for multi-sample single-cell RNA-seq datasets, such as:

- 10x Genomics output files
- Processed count matrices
- AnnData or Seurat-format objects
- Sample metadata tables

## Expected Output

The pipeline generates:

- Integrated single-cell object
- Quality-controlled and preprocessed data
- CellTypist-based cell type annotations
- CellPhoneDB-compatible input files
- CellPhoneDB ligand–receptor interaction results
- Basic visualization results such as UMAP plots and annotated cell clusters

## Notes

This repository is intended to provide a simple and reproducible workflow for standard single-cell RNA-seq preprocessing and cell–cell communication analysis.

The workflow can be adapted depending on the dataset structure, species, annotation model, and downstream biological questions.
