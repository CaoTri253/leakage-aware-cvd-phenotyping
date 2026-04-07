
# Notebooks

This directory contains the core computational pipeline for the cardiovascular phenotyping framework.

## 📄 Main Pipeline
- **`pipeline_Final_(Nộp).ipynb`**: This is the primary notebook for the study. It implements the "Leakage-Aware, Clinically Constrained" framework.

## 🛠 Notebook Structure
The pipeline is organized into the following logical sections to ensure clarity and reproducibility:

1. **Environment Setup**: Installation of necessary libraries (`XGBoost`, `Scikit-learn`, etc.) and Google Drive mounting.
2. **Data Loading**: Importing the `heart_diagnoses_all.csv` from the MIMIC-IV-Ext-Cardiac-Disease dataset.
3. **Clinical Pre-processing**: 
    - Filtering cases based on the 5-sequence diagnosis constraint.
    - Mapping ICD-9/ICD-10 codes to specific cardiovascular phenotypes.
4. **Leakage-Aware Feature Engineering**: Implementation of strategies to prevent data leakage between training and evaluation phases.
5. **Model Training**: Hyperparameter tuning and training using the XGBoost algorithm.
6. **Evaluation & Visualization**: Generation of performance metrics (Precision, Recall, F1-score) and clinical plots (Confusion Matrix, Feature Importance).

## 🚀 How to Run

###leakage-aware-cvd-phenotyping.ipynb Option 1: Google Colab (Recommended)
Click the badge in the root `README.md` or open the file directly in Colab. Ensure your Google Drive contains the required data at the path defined in `BASE_PATH_EXT`.

### Option 2: Local Environment
If running locally, you will need:
- Python 3.10+
- Jupyter Notebook or JupyterLab
- To update the `BASE_PATH_EXT` variable to your local data folder.

```bash
pip install -r ../requirements.txt
jupyter leakage-aware-cvd-phenotyping.ipynb
