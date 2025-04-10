
```markdown
# 🏡 Home Credit Default Risk - LGBM + CatBoost Ensemble Solution

This repository contains my solution for the [Home Credit Default Risk](https://www.kaggle.com/competitions/home-credit-default-risk) competition on Kaggle.

The goal of this competition is to predict the probability that an applicant will have difficulty repaying a loan. This solution applies LightGBM and CatBoost classifiers, using stratified K-Fold cross-validation and feature importance for model interpretation.

---

## 📁 Project Structure

```
home-credit-lgb-cat-ensemble/
├── notebooks/
│   └── home-credit-lgb-cat-ensemble-guo_32.ipynb  # Main notebook
├── output/
│   └── submission.csv                              # Final prediction file
├── README.md
└── requirements.txt
```

---

## 📊 Model Overview

- **Models used**:  
  - `LightGBMClassifier`  
  - `CatBoostClassifier`

- **Training strategy**:
  - Stratified K-Fold cross-validation (n_splits=5)
  - Averaging predictions from both models

- **Evaluation metric**:
  - AUC (Area Under the ROC Curve)

---

## 🛠️ Feature Engineering

- Selected top features based on importance scores
- Categorical encoding handled automatically by CatBoost and LightGBM
- Dropped uninformative or highly missing-value columns

---

## 🚀 How to Run

Install dependencies:
```bash
pip install -r requirements.txt
```

Then open the notebook:
```bash
jupyter notebook notebooks/home-credit-lgb-cat-ensemble-guo_32.ipynb
```

Or run it as a script (if converted to `.py`):
```bash
python notebooks/home-credit-lgb-cat-ensemble-guo_32.py
```

---

## 📈 Model Performance (CV)

| Model         | CV AUC Score |
|---------------|--------------|
| LGBM          | ~0.749       |
| CatBoost      | ~0.747       |
| Ensemble Avg  | **~0.752**   |

---

## 📦 Dependencies

```txt
pandas
numpy
scikit-learn
lightgbm
catboost
matplotlib
tqdm
```

---

## 📤 Submission

The final prediction is stored as:
```
output/submission.csv
```

This file can be submitted directly to Kaggle.

---

## 🧊 License

This project is licensed under the MIT License.
```

