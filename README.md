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
`xgboost`, `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `optuna`, `shap`.

**Core Pipeline Modules:**
- **Module A (Labs):** Biomarker extraction and sparsity filtering.
- **Module B (Text):** NLP-based feature extraction (TF-IDF) from clinical notes.
- **Module C (Cardiac):** Specialized Regex-based extraction for LVEF and ECG patterns.
- **Module D (Demographics):** Integrated from MIMIC-IV Core tables.

## 👥 Authors & Contributors

### Core Research Team
* **Dat Tan Nguyen** (Lead Researcher) 
  [![ORCID](https://img.shields.io/badge/ORCID-0009--0008--8301--4972-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0008-8301-4972)
  - *Taipei Medical University | Can Tho University*
* **Minh-Tri Cao** (Lead Developer) 
  [![ORCID](https://img.shields.io/badge/ORCID-0009--0005--9683--0053-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0005-9683-0053)
  - *Independent Biomedical Researcher | Freelance AI developer in Vietnam*
* **Minh Huu Nhat Le** - *Taipei Medical University*
* **Thu Minh Phung** [![ORCID](https://img.shields.io/badge/ORCID-0009--0006--5111--232X-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0006-5111-232X)
  - *Taipei Medical University | Can Tho University of Medicine and Pharmacy*

### Collaborating Investigators
* **Duy Viet Le** [![ORCID](https://img.shields.io/badge/ORCID-0009--0007--5015--6838-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0007-5015-6838)
  - *Uppsala University, Sweden*
* **Tan Phat Huynh** [![ORCID](https://img.shields.io/badge/ORCID-0009--0003--1650--713X-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0003-1650-713X)
  - *National Taiwan University of Science and Technology*
* **Ngoc-Nguyen Thi Nguyen** [![ORCID](https://img.shields.io/badge/ORCID-0009--0008--8425--7650-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0008-8425-7650)
  - *Can Tho Oncology Hospital*
* **Quang-Hien Kha** - *Taipei Medical University*

### Supervision & Corresponding Author
* **Nguyen Quoc Khanh Le** (Principal Investigator)
  - *Founder of AIBioMed Group, Taipei Medical University* - 📧 Email: [khanhlee@tmu.edu.tw](mailto:khanhlee@tmu.edu.tw)


---
## 📧 Contact

For inquiries regarding **clinical methodology, cohort selection, and research logic**, please contact:
* **Dat Tan Nguyen** (Lead Researcher): [d142114024@tmu.edu.tw](mailto:d142114024@tmu.edu.tw)

For inquiries regarding **technical implementation, code maintenance, and reproduction**, please contact:
* **Minh-Tri Cao** (Lead Developer): [minhtripro253@gmail.com](mailto:minhtripro253@gmail.com)

For **official collaboration and administrative matters**, please contact the Corresponding Author:
* **Nguyen Quoc Khanh Le** (Principal Investigator): [khanhlee@tmu.edu.tw](mailto:khanhlee@tmu.edu.tw)

## 📜 Citation
If you use this code or framework in your research, please cite our paper:

```bibtex
@article{nguyen2026leakage,
  title={A Leakage-Aware, Clinically Constrained Machine Learning Framework for Multi-Class Cardiovascular Phenotyping from EHR Data},
  author={Nguyen, Dat Tan and Cao, Minh-Tri and Le, Minh Huu Nhat and Phung, Thu Minh and Le, Duy Viet and Huynh, Tan Phat and Nguyen, Ngoc-Nguyen Thi and Kha, Quang-Hien and Le, Nguyen Quoc Khanh},
  journal={To be submitted},
  year={2026},
  url={https://github.com/CaoTri253/leakage-aware-cvd-phenotyping}
}
