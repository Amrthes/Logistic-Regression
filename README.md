# Wine Quality Prediction

## Overview

This project predicts **wine quality** based on its chemical properties using **Logistic Regression**. The dataset includes 200 samples with 6 features related to acidity, sugar, pH, alcohol, and density.

---

## Dataset

* **File:** `wine_quality.csv`
* **Shape:** 200 rows × 6 columns
* **Features:**

  * `acidity`
  * `sugar`
  * `pH`
  * `alcohol`
  * `density`
* **Target:** `quality` (wine score: 3–8)

---

## Data Preprocessing

* Checked for **null values & duplicates** → none found.
* Standardized features using **StandardScaler**.
* Split data into **train (80%)** and **test (20%)** with stratification.

---

## Modeling

* **Algorithm:** Logistic Regression (multinomial, lbfgs solver, max\_iter=500).
* **Evaluation Metrics:** Accuracy, F1 Score (macro & weighted), Confusion Matrix, Classification Report.

---

## Results

* **Accuracy:** 30%
* **Macro F1 Score:** 0.27
* **Weighted F1 Score:** 0.28

📊 **Confusion Matrix**

| True \ Pred | 3 | 4 | 5 | 6 | 7 | 8 |
| ----------- | - | - | - | - | - | - |
| **3**       | 2 | 0 | 1 | 1 | 2 | 0 |
| **4**       | 2 | 3 | 0 | 2 | 0 | 0 |
| **5**       | 0 | 2 | 2 | 1 | 2 | 0 |
| **6**       | 1 | 0 | 1 | 4 | 2 | 0 |
| **7**       | 2 | 0 | 2 | 1 | 1 | 0 |
| **8**       | 2 | 0 | 1 | 2 | 1 | 0 |

---

## Visualizations

* **Correlation Heatmap** for feature relationships.
* **Confusion Matrix Heatmap** to visualize classification errors.

---

## How to Run

1. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

2. Place `wine_quality.csv` in the working directory.
3. Run the Jupyter Notebook / script to reproduce results.

---

## Notes

* Logistic Regression gave **low accuracy** due to class imbalance & small dataset.
* Can improve using **Random Forest, XGBoost, or Neural Networks**.

