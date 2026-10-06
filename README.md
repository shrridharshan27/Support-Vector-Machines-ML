# ML Lab 07: Support Vector Machines (SVM)

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E.svg?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/pandas-150458.svg?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-013243.svg?logo=numpy&logoColor=white)](https://numpy.org/)

---

## Academic Details
- **Student Name:** Shrri Dharshan D R
- **Register Number:** 23BPS1090
- **Course Code:** BCSE209P
- **Course Title:** Machine Learning Laboratory
- **Faculty:** Dr. S. Shridevi
- **Institution:** School of Computer Science and Engineering (SCOPE), VIT Chennai

---

## Overview
This repository contains laboratory implementations and empirical evaluations of **Support Vector Machines (SVM)** for binary classification across medical diagnostic and document authentication datasets from the UCI Machine Learning Repository.

The laboratory explores maximal margin hyperplanes, hard-margin vs. soft-margin formulations (slack variables $\xi_i$ and the regularization parameter $C$), the kernel trick for mapping non-linearly separable data into higher-dimensional feature spaces (Linear, Polynomial, Radial Basis Function / RBF, Sigmoid), and support vector identification.

---

## Experiments & Datasets

### 1. Banknote Authentication Classification
- **Dataset:** Banknote Authentication Dataset ([UCI ID: 267](https://archive.ics.uci.edu/dataset/267))
- **Objective:** Classify banknotes as **Genuine** (`0`) or **Forged** (`1`) using continuous wavelet transform features extracted from high-resolution images (Variance, Skewness, Kurtosis, and Entropy).
- **Notebook:** [23BPS1090_ShrriDharshan_ML_Lab_SVM_BanknoteAuth.ipynb](./23BPS1090_ShrriDharshan_ML_Lab_SVM_BanknoteAuth.ipynb)
- **Data Directory:** `banknote_data/`
- **Techniques:** Standard feature scaling, kernel comparison (Linear, Poly, RBF), cost parameter $C$ sensitivity analysis, 2D decision boundary visualization, and support vector analysis.

### 2. Breast Cancer Wisconsin (Diagnostic)
- **Dataset:** Breast Cancer Wisconsin (Diagnostic) Dataset ([UCI ID: 17](https://archive.ics.uci.edu/dataset/17))
- **Objective:** Predict whether a breast mass tumor is **Malignant** (`M`) or **Benign** (`B`) from 30 real-valued cell nuclei features computed from digitized Fine Needle Aspirate (FNA) images.
- **Notebook:** [23BPS1090_ShrriDharshan_ML_Lab_SVM_BreastCancer.ipynb](./23BPS1090_ShrriDharshan_ML_Lab_SVM_BreastCancer.ipynb)
- **Data Directory:** `bc_data/`
- **Techniques:** Robust scaling, PCA dimensionality reduction for boundary contour projection, RBF kernel $\gamma$ and $C$ grid optimization, and clinical diagnostic sensitivity (minimizing False Negatives).

---

## Evaluation Metrics
- **Classification Accuracy & Balanced Accuracy**
- **Sensitivity / Recall:** Critical for medical diagnostics (detecting Malignant tumors)
- **Specificity & Precision:** Minimizing false alarms in authentication
- **F1-Score** (Macro and Weighted)
- **Receiver Operating Characteristic (ROC-AUC)**
- **Confusion Matrices** with normalized rate distributions
- **Support Vector Ratio:** Ratio of boundary-defining vectors to total sample size

---

## Repository Structure
```text
ML-Lab-07-Support-Vector-Machines-SVM/
├── 23BPS1090_ShrriDharshan_ML_Lab_SVM_BanknoteAuth.ipynb
├── 23BPS1090_ShrriDharshan_ML_Lab_SVM_BreastCancer.ipynb
├── banknote_data/
├── bc_data/
├── .gitignore
└── README.md
```

---

## How to Run
1. **Clone the repository:**
   ```bash
   git clone https://github.com/shrridharshan27/ML-Lab-07-Support-Vector-Machines-SVM.git
   cd ML-Lab-07-Support-Vector-Machines-SVM
   ```
2. **Install dependencies:**
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn ucimlrepo jupyter
   ```
3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
