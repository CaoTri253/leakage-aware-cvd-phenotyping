# Data Access and Preparation

This study utilizes the **MIMIC-IV-Ext-Cardiac-Disease (v1.0.0)**, a specialized extension of the MIMIC-IV database.

## 🔓 Data Access
This dataset is a restricted-access resource hosted on PhysioNet. To use the code in this repository, you must:
1. Have an approved PhysioNet account with completed CITI training.
2. Request access to the extension here: [https://physionet.org/content/mimic-iv-ext-cardiac-disease/1.0.0/](https://physionet.org/content/mimic-iv-ext-cardiac-disease/1.0.0/)

## 📁 Directory Structure & Setup
The pipeline is configured to read data from Google Drive. Please ensure your environment is structured as follows:

### 1. Google Drive Path
The dataset should be placed in this exact directory:
`/content/drive/MyDrive/MIMIC DATASET/mimic-iv-ext-cardiac-disease/`

### 2. Required File
Inside the above folder, ensure you have the primary dataset file:
- `heart_diagnoses_all.csv` (Main dataset used for case extraction and phenotyping)

```text
📦 MIMIC DATASET
 ┗ 📂 mimic-iv-ext-cardiac-disease
   ┗ 📜 heart_diagnoses_all.csv
