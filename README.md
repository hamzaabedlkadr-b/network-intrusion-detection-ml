# Network Intrusion Detection with Classical Machine Learning

This repository is a portfolio version of a machine learning project built on the NSL-KDD intrusion detection dataset. It compares classical supervised models in both binary and multiclass settings, with a focus on preprocessing, cross-validation, generalization, and class-imbalance behavior.

## What the project covers

- Binary classification: normal vs. attack traffic
- Multiclass classification: Normal, DoS, Probe, R2L, and U2R
- Shared preprocessing with one-hot encoding and standardization
- Hyperparameter tuning with stratified cross-validation
- Evaluation with accuracy, macro-F1, balanced accuracy, confusion matrices, ROC curves, and AUC

## Models compared

- Logistic Regression
- Softmax Regression
- Naive Bayes
- Decision Tree
- Random Forest

## Key results

| Setting | Best model | Highlights |
| --- | --- | --- |
| Binary classification | Decision Tree / Random Forest | Decision Tree reached the best macro-F1 (0.78), while Random Forest achieved the strongest ROC-AUC (0.959). |
| Multiclass classification | Random Forest | Best test accuracy (0.8803), best macro-F1 (0.6759), and best balanced accuracy (0.6765). |

Softmax Regression was also competitive in the multiclass setting, while Naive Bayes consistently struggled on minority classes because of its strong independence assumptions.

## Repository structure

- `binary.ipynb`: binary classification workflow
- `multiclass.ipynb`: multiclass classification workflow
- `report/main.tex`: polished project report source
- `report/main.pdf`: compiled project report
- `report/*.png`: figures used in the report

## Getting started

1. Create and activate a virtual environment.
2. Install dependencies with `pip install -r requirements.txt`.
3. Download the NSL-KDD files `KDDTrain+.txt` and `KDDTest+.txt`.
4. Place both dataset files in the repository root.
5. Open `binary.ipynb` or `multiclass.ipynb` and run the notebooks.

The notebooks were updated to use local relative paths instead of Colab-only `/content/...` paths.

## Notes for public sharing

- Raw dataset files are ignored from version control in `.gitignore`.
- LaTeX build artifacts and old submission bundle files are also ignored.
- The report text has been rewritten so it reads as an independent project report.

## Dataset

- NSL-KDD reference: <https://www.kaggle.com/datasets/hassan06/nslkdd?select=KDDTrain%2B.arff>
