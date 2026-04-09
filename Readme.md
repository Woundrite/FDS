# Foundations of Data Science Group Project

## Project Title

Multiple Models used on the TonIOT dataset

## Team

- Group: 8
- Members:

| Reg. No.   | Name                     |
| ---------- | ------------------------ |
| 23BCE10922 | ARTI SHARMA              |
| 23BCE10974 | RAUSHIK GUPTA            |
| 23BCE10977 | SHUBHAM SANDEEP BATWE    |
| 23BCE10985 | NIKHIL DHANANJAY BENDALE |
| 23BCE11009 | MANIKYA NARIYAL          |
| 23BCE11024 | AADYA CHAUHAN            |

All Members Contributed

## Project Summary

This project analyzes normal Windows telemetry data from the TON_IoT dataset to build a clean machine learning pipeline for:

- Data preprocessing and integration
- Exploratory data analysis
- Dimensionality reduction
- Predictive and anomaly detection modeling

The goal is to compare multiple machine learning approaches and document a reproducible workflow suitable for academic submission.

## Dataset

- Source: TON_IoT (Windows telemetry subset)
- Local data path: data/
- Files used:
    - win7_normal_1.csv
    - win7_normal_2.csv
    - win7_normal_3.csv
    - win10_normal_1.csv
    - win10_normal_2.csv
    - win10_normal_3.csv
    - win10_normal_4.csv

## Repository Structure

```
FDS/
|- preprocessing_svd_pca.ipynb
|- data_visualizations.ipynb
|- decision_tree_model.ipynb
|- KNN_Anomaly_detection_model.ipynb
|- linear_regression_model.ipynb
|- logistic_regression_model.ipynb
|- naIve_bayes_model.ipynb
|- Random_Forest_model.ipynb
|- Readme.md
|- data/
|- old/
|- output/
```

## Main Notebooks

- preprocessing_svd_pca.ipynb
    - Combines raw CSV files
    - Cleans column names and timestamps
    - Handles missing values and constant features
    - Performs PCA and Truncated SVD for feature reduction
- decision_tree_model.ipynb
    - Decision Tree based modeling and evaluation
- Random_Forest_model.ipynb
    - Random Forest model training and comparison
- logistic_regression_model.ipynb
    - Logistic Regression baseline and analysis
- naIve_bayes_model.ipynb
    - Gaussian Naive Bayes load-state classification and uncertainty analysis
- linear_regression_model.ipynb
    - Linear Regression experiments
- KNN_Anomaly_detection_model.ipynb
    - KNN-based anomaly detection experiments

## Latest Model Results (Load State Classification)

The project now includes confusion matrix, ROC, and Precision-Recall visualizations for all classification notebooks.

| Model                | Test Accuracy | CV Accuracy (if available) | ROC AUC (Active / Idle / Stressed)                               |
| -------------------- | ------------- | -------------------------- | ---------------------------------------------------------------- |
| Decision Tree        | 0.9366        | -                          | Added in notebook (latest cell not re-executed in current state) |
| Logistic Regression  | 0.8839        | 0.8846 +/- 0.0048          | 0.954 / 0.999 / 0.952                                            |
| Random Forest        | 0.9341        | 0.9286 +/- 0.0047          | 0.985 / 1.000 / 0.984                                            |
| Gaussian Naive Bayes | 0.5628        | -                          | 0.702 / 0.966 / 0.737                                            |

Naive Bayes PR values (AP) from latest run:

- Active: 0.686
- Idle: 0.401
- Stressed: 0.467

## Data Processing Workflow

1. Load all source Windows CSV files.
2. Normalize and clean feature names.
3. Parse timestamp and convert valid features to numeric values.
4. Merge datasets using shared columns.
5. Fill missing values (median strategy for numeric columns).
6. Remove constant (non-informative) features.
7. Apply PCA and Truncated SVD to reduce dimensionality.
8. Train and compare multiple machine learning models.

## Output Artifacts

- Cleaned combined dataset and reduced datasets generated in notebook workflow
- Model-specific results in respective notebooks

## Environment and Dependencies

Recommended environment:

- Python 3.9+
- Jupyter Notebook or Google Colab

Key Python libraries:

- pandas
- numpy
- matplotlib
- scikit-learn

Install dependencies with:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

## How to Run

1. Open this project folder in VS Code, Jupyter, or Colab.
2. Ensure data files exist in data/.
3. Run preprocessing_svd_pca.ipynb first to prepare cleaned and reduced data.
4. Run model notebooks one by one for training and evaluation.
5. Compare metrics and observations across models.

## Acknowledgment

This project uses the TON_IoT dataset for educational and research purposes as part of the Foundations of Data Science course work.
