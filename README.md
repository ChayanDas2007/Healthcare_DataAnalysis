# Healthcare Data Analysis: Breast Cancer Diagnosis Prediction

**IBM SkillsBuild Internship — Data Analytics Project**

## 📌 Overview

This project analyzes the **Breast Cancer Wisconsin (Diagnostic) Data Set** to understand how
cell-nuclei measurements from breast mass biopsies relate to tumor diagnosis, and builds
classification models to predict whether a tumor is **Malignant** or **Benign**.

## 🎯 Objectives

- Perform exploratory data analysis (EDA) to understand feature distributions and relationships
- Identify which features are most strongly associated with malignant diagnoses
- Build and compare two classification models: Logistic Regression and Random Forest
- Evaluate model performance using accuracy, precision, recall, F1-score, and ROC-AUC

## 🗂️ Dataset

| | |
|---|---|
| **Source** | `sklearn.datasets.load_breast_cancer` (originally UCI Machine Learning Repository) |
| **Records** | 569 |
| **Features** | 30 numeric features (mean, standard error, and "worst" values of 10 cell-nuclei characteristics) |
| **Target** | Diagnosis — Malignant (0) or Benign (1) |
| **Missing values** | None |

## 📁 Project Structure

```
├── healthcare_data_analysis.ipynb   # Jupyter notebook (main deliverable — run this)
├── healthcare_data_analysis.py      # Equivalent standalone Python script
├── requirements.txt                 # Python dependencies
├── README.md                        # This file
├── Project_Report.docx              # Full written project report
├── breast_cancer_data.csv           # Generated on run — the raw dataset
├── metrics.json                     # Generated on run — model performance summary
└── figures/                         # Generated on run — all charts (EDA + evaluation)
```

## ⚙️ Setup & Installation

1. **Clone/download this project** and open a terminal in the project folder.

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## ▶️ How to Run

**Option A — Jupyter Notebook (recommended, shows all outputs inline):**
```bash
jupyter notebook healthcare_data_analysis.ipynb
```
Then run all cells (Cell → Run All).

**Option B — Python script:**
```bash
python healthcare_data_analysis.py
```
This prints results to the console and saves all charts to the `figures/` folder.

## 🧪 Methodology

1. **Data Loading & Understanding** — load the dataset, check shape, types, and missing values
2. **EDA** — class balance, correlation heatmap, boxplots of key features by diagnosis, scatter plots
3. **Preprocessing** — train/test split (80/20, stratified) and feature scaling (`StandardScaler`)
4. **Modeling** — Logistic Regression and Random Forest classifiers
5. **Evaluation** — accuracy, precision, recall, F1-score, ROC-AUC, confusion matrix, feature importance

## 📊 Results Summary

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | 98.2% | 98.6% | 98.6% | 98.6% | 0.995 |
| Random Forest | 95.6% | 95.9% | 97.2% | 96.6% | 0.993 |

*(Exact values may vary slightly by environment due to library versions; random_state is fixed for reproducibility.)*

## 🔑 Key Insights

- Features describing **cell concavity, area, and perimeter** are the strongest predictors of malignancy.
- Both models achieve high recall on malignant cases — important in healthcare, where false negatives
  (missed cancer diagnoses) carry the highest risk.
- Logistic Regression slightly outperformed Random Forest on this particular dataset/split.

## 🚀 Future Improvements

- Hyperparameter tuning with `GridSearchCV` / `RandomizedSearchCV`
- K-fold cross-validation for more robust performance estimates
- Additional models (SVM, XGBoost, Gradient Boosting)
- Validation on external/real-world clinical data

## 📄 License

This project uses a publicly available dataset for educational purposes as part of the
IBM SkillsBuild Internship program.
