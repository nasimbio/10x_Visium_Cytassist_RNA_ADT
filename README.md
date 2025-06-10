# 🧬 Gene and Protein Expression Profiling from FFPE Tissues — Visium CytAssist

This project applies **10x Genomics Visium CytAssist** spatial transcriptomics technology on FFPE human tissue, integrating **RNA** and **protein (antibody-based)** expression to investigate spatially resolved molecular signatures. Downstream analysis includes RNA-protein integration and **deconvolution** using a single-cell reference dataset.

---

## 📘 Project Overview

Spatial transcriptomics data generated with **10x Visium CytAssist** platform enables simultaneous profiling of **mRNA** and **protein** markers in FFPE tissue sections. This project aims to:

- Perform separate analysis of spatial RNA and protein expression
- Visualize clustering and spatial patterns of cellular compartments
- Infer cell type composition in each spot by leveraging a matched scRNA-seq reference through **SPOTlight deconvolution**

---

## 📊 Analysis Tasks

### **Task 1: Spatial RNA and Protein Analysis**

#### 🔹 RNA Modality
- Load spatial RNA gene expression matrix into a Seurat object
- Perform standard preprocessing steps:
  - Quality control
  - Normalization via SCTransform
  - Dimensionality reduction (PCA)
  - Clustering and UMAP embedding
  - SpatialFeaturePlot and cluster marker analysis

#### 🔹 Protein Modality
- Load spatial protein (antibody-derived) expression data
- Normalize using **CLR (centered log-ratio)** method
- Compare and overlay protein-level expression with RNA clusters


---

### **Task 2: Cell Type Deconvolution with SPOTlight**

- Preprocess a well-annotated **single-cell RNA-seq reference** dataset (e.g., filtering, normalization, and selection of variable genes)
- Use the **SPOTlight R package** to deconvolute spatial RNA data:
  - Estimate proportion of reference-defined cell types in each Visium spot
  - Visualize spatial distribution of predicted cell types
  - Identify region-specific enrichment or depletion

---

# 💡 Notes

- Raw data is not publicly available due to client ownership and confidentiality.
- Some example outputs plots are organized by task in the `output/` folder.
- This project is designed for both reproducibility and clarity.

---

## 📬 Contact

*Author:* Nasim Rahmatpour 
*Email:* nasimrahmatpour1@gmail.com 
*GitHub:* (https://github.com/nasimbio)

