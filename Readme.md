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
|- Copy_of_Data_Science.ipynb
|- decision_tree_model.ipynb
|- KNN_Anomaly_detection_model.ipynb
|- linear_regression_model.ipynb
|- logistic_regression_model.ipynb
|- Random_Forest_model.ipynb
|- Readme.md
|- data/
|- old/
|- output/
```

## Main Notebooks

- Copy_of_Data_Science.ipynb
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
- linear_regression_model.ipynb
  - Linear Regression experiments
- KNN_Anomaly_detection_model.ipynb
  - KNN-based anomaly detection experiments

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
3. Run Copy_of_Data_Science.ipynb first to prepare cleaned and reduced data.
4. Run model notebooks one by one for training and evaluation.
5. Compare metrics and observations across models.

## Academic Submission Notes

- Ensure all team member names and IDs are added in the Team section.
- Keep outputs and notebook results up to date before submission.
- Export notebooks to PDF/HTML if required by your instructor.

## Acknowledgment

This project uses the TON_IoT dataset for educational and research purposes as part of the Foundations of Data Science course work.
