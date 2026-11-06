# bladder-cancer-ML
Initial commit of bladder cancer ML project


# =====================================================================
# SCRIPT TO GENERATE GITHUB README.md
# =====================================================================

readme_text <- "# Predicting Neoadjuvant Chemotherapy Response in Bladder Cancer

## Project Overview
This repository contains a complete bioinformatics and machine learning pipeline designed to predict the response to Neoadjuvant Chemotherapy (NAC) in Muscle-Invasive Bladder Cancer (MIBC). By integrating transcriptomic RNA-seq data from two independent GEO cohorts (**GSE212810** and **GSE247185**), we identified a robust, multi-gene biomarker signature.

## Analytical Pipeline
1. **Data Cleaning & Preprocessing:** Handled metadata discrepancies and identified/removed an extreme Squamous outlier (Sample 1) to prevent model overfitting.
2. **Differential Expression (DESeq2):** Identified genes significantly associated with pathological complete response (pCR).
3. **Machine Learning (XGBoost & Lasso):** Applied Lasso regression and XGBoost to select the most predictive features from a 65-gene overlapping signature.
4. **Clinical Validation:** Built a parsimonious 2-gene logistic regression model, achieving an **ROC AUC of 0.80** and a **Sensitivity of 90%**.

## Key Biomarkers Identified


## Repository Contents
- `Bladder_Cancer_Project.RData`: The complete saved R workspace (data, models, variables).
- `Bladder_Cancer_Code_History.R`: The full history of R commands executed.
- `Figure1_Publication_Quality.png`: Cohort details and analytical pipeline flowchart.
- `Figure2_Nature_Style_Volcano.png`: Differential expression volcano plots.
- `Figure3_Nature_Style_GO.png`: Gene Ontology (GO) pathway analysis.
- `Figure4_ROC_Curve_Updated.jpg`: ROC curve validating the 2-gene signature.
- `Figure5_Biomarker_Barplot.png`: Expression levels of the key biomarkers.

## How to Reproduce
1. Clone this repository to your local machine.
2. Open R/RStudio and set your working directory to the cloned folder.
3. Load the saved workspace by running: 
   `load('Bladder_Cancer_Project.RData')`
4. You can now access all dataframes (e.g., `dds_39`, `res_39`, `xgb_model_clean`) directly in your R environment.

## Author
Mandana AmeliMojarad

# Write the text to a file named README.md
writeLines(readme_text, "README.md")

print("SUCCESS! 'README.md' has been created in your folder.")
print("Upload this file to GitHub along with your other files.")
