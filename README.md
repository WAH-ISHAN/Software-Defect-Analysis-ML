# 🏥 Electronic Health Records (EHR) Quality Scorecard

> A Machine Learning-based tool to evaluate the **Research Readiness** of Electronic Health Record data, helping researchers reduce bias and improve the accuracy of healthcare AI models.

---

## 📌 Project Overview

- Electronic Health Records (EHR) are essential for modern healthcare research, yet they often suffer from issues such as missing values, inconsistencies, and incomplete documentation.
- This project introduces a **Machine Learning-based Quality Scorecard** to evaluate the *Research Readiness* of EHR data.
- Records are classified as **reliable** or **unreliable** before they reach the analysis stage.
- This tool helps researchers reduce bias and improve the accuracy of healthcare AI models.

---

## 🚀 Key Features

- **Feature Engineering** — Transforms raw EHR tables (patients, observations, encounters) into meaningful documentation density ratios.
- **Research Readiness Scoring** — A custom proxy indicator built using clinical documentation principles.
- **Predictive Modeling** — Utilizes Logistic Regression (optimized with L2 regularization) to classify data quality.
- **Bias Mitigation** — Implements Gaussian noise and median-based thresholds to ensure the model learns true patterns rather than overfitting.

---

## 📊 Methodology

The project follows a structured ML lifecycle:

1. **Data Collection** — Used synthetic EHR data ([Synthea](https://github.com/synthetichealth/synthea)) to ensure privacy while maintaining realism.
2. **Preprocessing**
   - Log transformation (`X' = ln(1 + X)`) to handle skewed distributions.
   - `StandardScaler` normalization for feature scaling.
3. **Model Selection** — Evaluated Logistic Regression, Decision Trees, and Random Forest.
4. **Evaluation** — Achieved a stable cross-validation accuracy of **~80.4%** using Logistic Regression.

---

## 📈 Performance Summary

| Metric    | Value  |
|-----------|--------|
| Accuracy  | 81.4%  |
| Precision | 84.7%  |
| Recall    | 76.6%  |
| F1-Score  | 80.4%  |

---

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Tools:** Google Colab / Jupyter Notebook, GitHub

---

## 📂 Repository Structure

```
├── notebooks/          # Google Colab/Jupyter notebook with full code
├── data/               # Aggregated dataset info and source links
├── results/            # Confusion matrix and ROC curve visualizations
├── Software_Defect_Analysis_ML.ipynb   # Main analysis notebook
├── electronic-health-records-quality-scorecard-Report.pdf
└── README.md
```

---

## 👥 Team Members — COHNDSE251F

- **W D Y N Gunawardana** (041)
- **W A H Ishan** (042)
- **W W Thilini Piyumika** (058)
- **P A R Sahas Suraweera** (059)

**Guided by:** Mr. Gihan Weerasekara (NIBM)

---

## 📜 References

- Weiskopf, N. G., & Weng, C. (2013). *Methods and dimensions of EHR data quality assessment.* Journal of the American Medical Informatics Association.
- Synthea Open Source EHR: [https://github.com/synthetichealth/synthea](https://github.com/synthetichealth/synthea)
