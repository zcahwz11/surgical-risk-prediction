# Surgical Risk Prediction Models

This repository contains the analysis code for the study "Machine Learning-Based Prediction of 30-, 60-, and 90-day Postoperative Mortality and Major Complications: An 11-Year Population-Based Cohort Study in Hong Kong."

## Scope

The repository contains the notebooks used for:

- 10 perioperative full models;
- 10 reduced 13-predictor preoperative models;
- eight complication-specific models;
- AUROC, AUPRC, Brier score, and calibration evaluation;
- logistic recalibration;
- SHAP model interpretation; and
- age- and ASA-based subgroup evaluation.

Source-data extraction, record linkage, database management, and data-cleaning code are not included. The analyses begin with analysis-ready tables.

## Repository structure

```text
code_submission/
|-- README.md
|-- LICENSE
|-- CITATION.cff
|-- environment.yml
|-- .gitignore
`-- notebooks/
    |-- 01_full_models/
    |-- 02_reduced_models/
    |-- 03_complication_specific_models/
    |-- 04_model_evaluation/
    |-- 05_recalibration/
    `-- 07_subgroup_analysis/
```

SHAP analysis is contained within each full- and reduced-model notebook because it was performed as part of the corresponding model workflow. Complication-specific evaluation is likewise contained within each complication-specific model notebook.

## Environment

```bash
conda env create -f environment.yml
conda activate surgery-risk-prediction
```


## Data availability

The SOMIP patient-level data cannot be redistributed because of institutional governance and patient-confidentiality requirements. No patient-level data, patient-level predictions, or fitted model objects are included in this repository.

