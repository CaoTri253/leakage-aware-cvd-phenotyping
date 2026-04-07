# A Leakage-Aware, Clinically Constrained Machine Learning Framework for Multi-Class Cardiovascular Phenotyping from EHR Data

Official implementation for our research on multi-class cardiovascular disease prediction. This framework integrates specialized cardiac extensions with core Electronic Health Records (EHR) from the MIMIC-IV database.

## 🚀 Reproduction
You can reproduce the entire pipeline (from feature engineering to model evaluation) directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/114wWYSNA8vzeOpkITXqlRFIwOlwpqLWX?usp=sharing)

## 📁 Repository Structure
* `notebooks/`: Contains the core research pipeline (`.ipynb`) with modules for Lab, Text, Cardiac, and Demographic features.
* `data/`: Comprehensive guide on accessing and structuring **MIMIC-IV v3.1** and the **Cardiac Extension** dataset.
* `results/`: High-resolution visualizations including Optuna history, SHAP interpretability plots, and multi-class performance metrics.

## 📊 Dataset & Data Integration
This project utilizes a multi-source data integration approach:
1. **MIMIC-IV-Ext-Cardiac-Disease (v1.0.0)**: Used for extracting specific cardiac diagnoses, lab events, microbiology, and clinical reports.
   - [PhysioNet Extension Link](https://physionet.org/content/mimic-iv-ext-cardiac-disease/1.0.0/)
2. **MIMIC-IV v3.1**: Used for core patient demographics (Age, Gender, Race) to ensure clinical validity.
   - [PhysioNet Core Link](https://physionet.org/content/mimiciv/3.1/)

## 🛠 Prerequisites & Modules
The pipeline is built on Python 3.10+ and requires the following libraries:
`xgboost`, `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `optuna`, `shap`.

**Core Pipeline Modules:**
- **Module A (Labs):** Biomarker extraction and sparsity filtering.
- **Module B (Text):** NLP-based feature extraction (TF-IDF) from clinical notes.
- **Module C (Cardiac):** Specialized Regex-based extraction for LVEF and ECG patterns.
- **Module D (Demographics):** Integrated from MIMIC-IV Core tables.

## 📧 Contact
**Cao Trí** - Independent Biomedical Researcher  
**ORCID:** [0009-0005-9683-0053](https://orcid.org/0009-0005-9683-0053)  
**Email:** minhtripro253@gmail.com
