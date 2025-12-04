Single-Cell RNA-Seq Analysis of Bone Marrow Using Scanpy

This project reproduces a complete single-cell RNA-seq analysis pipeline using Scanpy, applied to a bone marrow dataset (derived from CZI and adapted for this task).
The goal is to process the dataset from raw counts to biologically meaningful cell type clusters and interpret the immune landscape.

Project Workflow

This notebook implements the standard Scanpy workflow:

Quality Control (QC)

Filtering of cells & genes

Normalization & log transformation

Highly Variable Gene (HVG) selection

PCA dimensionality reduction

Neighbor graph construction

Leiden clustering

UMAP visualization

Marker-based cell type annotation (using PanglaoDB via decoupler)

Biological interpretation of the tissue & immune state

 Key Results

14 immune clusters identified

Including:

T cells (naive & memory)

NK cells

γδ T cells

B cells (naive & transitional)

Plasma cells (mature)

Monocytes

Dendritic cells

Megakaryocytes / Platelets

Tissue Identity

The dataset strongly resembles bone marrow, supported by:

Megakaryocyte signatures

Multiple B-cell maturation stages

Plasma cell enrichment

Lymphocyte diversity (γδ T, NK)

Patient Immune State

The cell population distribution suggests viral-like immune activation, driven by:

NK cell expansion

Memory T-cell enrichment

Plasmacytoid dendritic cells

No neutrophil spike (not bacterial)

Repository Structure
├── Stage_2_Notebook.ipynb     # Main analysis notebook
├── README.md                   # Project summary & instructions


 How to Run the Notebook
Requirements (install inside Colab or local environment):
pip install scanpy decoupler omnipath anndata

To run:

Open the notebook in Google Colab or Jupyter Notebook

Upload the dataset file .h5ad

Run the cells sequentially




UMAP & cluster annotations will be generated automatically
