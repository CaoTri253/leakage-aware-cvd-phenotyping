# Data Access and Preparation (Comprehensive)

This study integrates two primary data sources: the **MIMIC-IV v3.1** base dataset and the **MIMIC-IV-Ext-Cardiac-Disease (v1.0.0)** extension.

## 🔓 Data Access
Both datasets are restricted-access resources hosted on PhysioNet. To run this pipeline, you must:
1. Have an approved PhysioNet account with completed CITI training.
2. Request access to **MIMIC-IV v3.1**: [Link](https://physionet.org/content/mimiciv/3.1/)
3. Request access to **MIMIC-IV-Ext-Cardiac-Disease**: [Link](https://physionet.org/content/mimic-iv-ext-cardiac-disease/1.0.0/)

## 📁 Required File Structure & Setup
The pipeline is configured to look for data in the following Google Drive paths. Please ensure your files are organized as follows:

### 1. Cardiovascular Extension Data (`BASE_PATH_EXT`)
Path: `/content/drive/MyDrive/MIMIC DATASET/mimic-iv-ext-cardiac-disease/`
Required files for feature extraction:
- `heart_diagnoses_all.csv`: Main cohort file for case selection.
- `heart_labevents_first_lab.csv`: Raw lab results for biomarkers (Module 2.1).
- `heart_diagnoses.csv`: Contains clinical notes, HPI, and ECG/Echo reports (Module 2.2).
- `heart_microbiologyevents.csv`: Microbiology culture results (Module 2.5).

### 2. MIMIC-IV Core Data (`MIMIC_IV_PATH`)
Path: `/content/drive/MyDrive/MIMIC DATASET/mimic-iv-3.1/hosp/`
Required for patient demographics (Module 2.4):
- `patients.csv.gz`: For gender and anchor age.
- `admissions.csv.gz`: For admission times and ethnicity (race).

---

## 🛠 Feature Engineering Modules
The pipeline extracts features across five specialized modules:
1. **[LABS]**: Extracts first lab events and filters for sparsity (>1% prevalence).
2. **[TEXT]**: Performs TF-IDF vectorization (top 300 keywords) from clinical notes and reports.
3. **[CARDIAC]**: Uses specialized Regex logic to extract **LVEF**, **Atrial Fibrillation (AFib)**, **ST-Elevation**, and **Sinus Rhythm**.
4. **[DEMO]**: Processes Age, Gender, and One-hot encoded Race groups.
5. **[MICRO]**: Processes microbiology organisms and culture results.

## ⚖️ Ethical & Audit Information
Usage of this data follows the PhysioNet Credentialed Health Data Use Agreement. Please do not re-distribute the data files in this repository.
---
*Note: In compliance with HIPAA and PhysioNet DUA, no patient-level data is redistributed in this repository.*
