# ceRNA Network Validation in Clear Cell Renal Cell Carcinoma (KIRC)

This repository contains a computational pipeline for validating the prognostic significance of a long non-coding RNA (lncRNA) mediated competitive endogenous RNA (ceRNA) network in Kidney Renal Clear Cell Carcinoma (KIRC) using TCGA data.

## Features
- **Data Acquisition**: Automated downloading of TCGA-KIRC transcriptomic, clinical, and survival data from GDC and Xena Hubs.
- **Multivariable Cox PH Analysis**: Evaluation of lncRNAs as independent prognostic markers adjusted for Age, Pathologic Stage, and Tumor Purity.
- **Partial Correlation Analysis**: Statistical validation of lncRNA-miRNA-mRNA interactions adjusted for ESTIMATE scores (tumor purity).
- **Survival Visualization**: Kaplan-Meier plots for high vs. low expression groups.

## Key Findings (Example: HSPA7)
- **Hazard Ratio (HR)**: 1.54 (p < 0.001), indicating HSPA7 is a robust high-risk biomarker.
- **Regulatory Mechanism**: Significant partial correlation between MIR6772 and CTLA4 (r = -0.24, p < 0.001) supports the ceRNA sponge hypothesis.

## Requirements
- Python 3.x
- `pandas`, `numpy`, `lifelines`, `pingouin`, `matplotlib`, `requests`

## Usage
Simply run the provided Jupyter Notebook. The script will automatically handle data downloading and preprocessing. Note: `idmap.xlsx` is required for gene symbol mapping.
