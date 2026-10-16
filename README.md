# Tox21 Toxicity Prediction

> 📄 **Official Implementation**: This repository contains the official implementation and codebase for the research paper:  
> **"Developing Computational Toxicology Models to Assess the Risk of Environmental Pollutants on Ecosystem Health"**  
> Published & Presented at the **[2025 IEEE 6th India Council International Subsections Conference (INDISCON)](https://ieeexplore.ieee.org/xpl/conhome/11251510/proceeding)**, Rourkela, India.  
> **Published by IEEE** | **DOI**: [10.1109/INDISCON66021.2025.11254833](https://doi.org/10.1109/INDISCON66021.2025.11254833)  
> **Electronic ISBN**: `979-8-3315-1504-1` | **Print on Demand (PoD) ISBN**: `979-8-3315-1505-8`

[![Paper](https://img.shields.io/badge/Paper-IEEE%20%7C%20INDISCON%202025-blue)](https://doi.org/10.1109/INDISCON66021.2025.11254833)
[![DOI](https://img.shields.io/badge/DOI-10.1109%2FINDISCON66021.2025.11254833-005691)](https://doi.org/10.1109/INDISCON66021.2025.11254833)
[![Conference](https://img.shields.io/badge/IEEE-INDISCON%202025-00629B)](https://ieeexplore.ieee.org/xpl/conhome/11251510/proceeding)
[![Python](https://img.shields.io/badge/Python-3.8%2B-brightgreen)]()
[![RDKit](https://img.shields.io/badge/RDKit-Cheminformatics-teal)]()
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)]()

---

## 📌 Overview
This project focuses on predicting the toxicity of chemical compounds to assess the risk of environmental pollutants on ecosystem health using machine learning and *in silico* computational toxicology techniques.

By leveraging molecular structures represented as **SMILES (Simplified Molecular Input Line Entry System)** strings from the **Tox21 dataset**, the models extract essential chemical descriptors (such as Molecular Weight, Heavy Atom Count, Rotatable Bonds, and LogP) and learn predictive patterns to classify compounds as **toxic** or **non-toxic**.

---

## 🔬 Key Features & Methodology
- **Molecular Descriptor Extraction**: Computes physicochemical properties from SMILES strings using **RDKit** (Molecular Weight, Heavy Atom Count, Num Rotatable Bonds, LogP).
- **Class Imbalance Mitigation**: Utilizes systematic resampling/oversampling to balance active (toxic) and inactive (non-toxic) chemical samples.
- **Machine Learning Classifiers**: Evaluates multiple machine learning models including:
  - **Random Forest (RF)**
  - **Support Vector Machine (SVM)**
  - **K-Nearest Neighbors (KNN)**
  - **Self-Organizing Neural Network (SNN / MiniSom)**
  - **Soft-Voting Ensemble Model** (combining RF, KNN, and SVM)
- **High-Performance Results**: Ensemble and tree-based models achieve high classification accuracy and F1 scores (~96–97%), providing reliable toxicity screening for environmental pollutants.

---

## 📂 Repository Structure

```text
Toxicity_Prediction/
│
├── Camera-ready code.ipynb    # Full Jupyter notebook with preprocessing, feature extraction, ML models, and evaluation
├── tox21.csv                  # Tox21 dataset containing SMILES strings and biological toxicity labels
├── BIO REPORT TEAM 5.pdf      # Detailed research project report
└── README.md                  # Project documentation & publication details
```

---

## 📊 Experimental Results

| Model | Accuracy | ROC-AUC / F1 | Key Notes |
| :--- | :---: | :---: | :--- |
| **Random Forest** | **0.96** | **0.96** (ROC-AUC) | Exceptional precision & recall across classes |
| **Ensemble Model (Voting)** | **0.97** | **0.97** (F1-score) | Soft-voting across RF, KNN, and SVM |
| **K-Nearest Neighbors (KNN)** | 0.80 | 0.89 (ROC-AUC) | High recall (0.94) on toxic compound identification |
| **Support Vector Machine (SVM)** | 0.71 | 0.78 (ROC-AUC) | Balanced sensitivity with RBF kernel |
| **Self-Organizing Map (SNN)** | 0.69 | 0.69 (F1-score) | Topological feature mapping via MiniSom |

---

## 🚀 Getting Started

### Prerequisites
Make sure you have Python 3.8+ installed along with the required libraries:

```bash
pip install numpy pandas scikit-learn rdkit minisom
```

### Running the Code
Open and run the notebook in Jupyter Notebook, JupyterLab, or VS Code:

```bash
jupyter notebook "Camera-ready code.ipynb"
```

---

## 🌍 Applications
- **Predicting Environmental Toxicity**: Assessing harmful impacts of chemical pollutants on ecological systems.
- **High-Throughput In Silico Screening**: Reducing dependency on animal testing through computational bioassays.
- **Regulatory Decision Support**: Helping environmental agencies screen emerging contaminants.

---

## 📜 Publication & Conference Details

- **Title**: *Developing Computational Toxicology Models to Assess the Risk of Environmental Pollutants on Ecosystem Health*
- **Conference**: [2025 IEEE 6th India Council International Subsections Conference (INDISCON)](https://ieeexplore.ieee.org/xpl/conhome/11251510/proceeding)
- **Location**: Rourkela, India
- **Publisher**: IEEE
- **DOI**: [10.1109/INDISCON66021.2025.11254833](https://doi.org/10.1109/INDISCON66021.2025.11254833)
- **Electronic ISBN**: `979-8-3315-1504-1`
- **Print on Demand (PoD) ISBN**: `979-8-3315-1505-8`

---

## 📜 License & Usage
This project is intended for **academic and research purposes**.

