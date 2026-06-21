# 🏦 Home Credit Default Risk Prediction

## 📌 Project Type
Project-Based Internship – Home Credit Indonesia (Data Scientist)

## 📊 Overview

Project ini merupakan implementasi machine learning untuk memprediksi risiko gagal bayar (*credit default risk*) pada pengajuan pinjaman menggunakan dataset Home Credit.

Tujuan utama project ini adalah membangun model klasifikasi yang mampu mengidentifikasi nasabah dengan risiko gagal bayar lebih tinggi sehingga dapat mendukung proses credit scoring secara lebih objektif dan berbasis data. Selain itu, model diharapkan dapat membantu mengurangi penolakan terhadap calon nasabah yang sebenarnya memiliki kemampuan untuk melunasi pinjaman.

Project dikembangkan secara end-to-end mulai dari exploratory data analysis (EDA), data cleaning, feature engineering, data preprocessing, hyperparameter tuning, model evaluation, hingga prediksi probabilitas default pada data testing.

---

## 🎯 Objectives

- Memahami karakteristik dataset dan distribusi target.
- Melakukan data cleaning dan preprocessing sebelum proses pemodelan.
- Mengembangkan fitur-fitur yang dapat meningkatkan performa model.
- Membangun dan membandingkan dua algoritma machine learning, yaitu Logistic Regression dan XGBoost.
- Melakukan hyperparameter tuning menggunakan RandomizedSearchCV.
- Mengevaluasi performa model menggunakan ROC-AUC dan Log Loss.
- Mengidentifikasi fitur-fitur yang paling berpengaruh terhadap prediksi risiko gagal bayar.
- Menghasilkan prediksi probabilitas default pada data testing.

---

## ⚙️ Machine Learning Pipeline

1. Data Understanding
2. Exploratory Data Analysis (EDA)
3. Data Cleaning
4. Feature Engineering
5. Train-Validation Split
6. Missing Value Imputation
7. Outlier Handling (Winsorization)
8. Feature Encoding & Scaling
9. Class Imbalance Handling (SMOTE)
10. Model Training
11. Hyperparameter Tuning
12. Model Evaluation
13. Feature Importance Analysis
14. Prediction on Test Dataset

---

## 🛠️ Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)
- XGBoost

---

## 🤖 Machine Learning Models

Dua algoritma yang digunakan pada project ini adalah:

- **Logistic Regression**
- **XGBoost Classifier**

Hyperparameter tuning dilakukan menggunakan **RandomizedSearchCV** dengan **Stratified 5-Fold Cross Validation**.

---

## 📈 Model Performance Benchmark

### Best Hyperparameters

| Model | Best Parameters |
|---------|----------------|
| Logistic Regression | `C = <<ISI SETELAH RUN>>`, `Penalty = <<ISI SETELAH RUN>>`, `Solver = saga` |
| XGBoost | `n_estimators = <<ISI SETELAH RUN>>`, `max_depth = <<ISI SETELAH RUN>>`, `learning_rate = <<ISI SETELAH RUN>>`, `subsample = <<ISI SETELAH RUN>>`, `colsample_bytree = <<ISI SETELAH RUN>>`, `scale_pos_weight = <<ISI SETELAH RUN>>` |

### 5-Fold Cross Validation

| Algorithm | Mean ROC-AUC | Mean Log Loss |
|------------|-------------:|--------------:|
| Logistic Regression | `<<ISI SETELAH RUN>>` | `<<ISI SETELAH RUN>>` |
| XGBoost | `<<ISI SETELAH RUN>>` | `<<ISI SETELAH RUN>>` |

Evaluasi dilakukan menggunakan **Stratified 5-Fold Cross Validation** untuk memperoleh estimasi performa model yang lebih stabil dan mengurangi risiko overfitting.

### Validation Set Performance

| Algorithm | ROC-AUC | Log Loss |
|------------|--------:|---------:|
| Logistic Regression | `<<ISI SETELAH RUN>>` | `<<ISI SETELAH RUN>>` |
| XGBoost | `<<ISI SETELAH RUN>>` | `<<ISI SETELAH RUN>>` |

Berdasarkan hasil evaluasi di atas, model **`<<ISI SETELAH RUN>>`** dipilih sebagai model terbaik karena menghasilkan kombinasi **ROC-AUC yang lebih tinggi** dan **Log Loss yang lebih rendah**, sehingga memiliki kemampuan yang lebih baik dalam membedakan kelas serta menghasilkan probabilitas prediksi yang lebih akurat.
## 🔍 Top 6 Feature Importance

Berikut enam fitur dengan kontribusi terbesar berdasarkan model terbaik:

| Rank | Feature |
|------|---------|
| 1 | `<<ISI SETELAH RUN>>` |
| 2 | `<<ISI SETELAH RUN>>` |
| 3 | `<<ISI SETELAH RUN>>` |
| 4 | `<<ISI SETELAH RUN>>` |
| 5 | `<<ISI SETELAH RUN>>` |
| 6 | `<<ISI SETELAH RUN>>` |

Analisis feature importance membantu memahami faktor-faktor yang paling memengaruhi prediksi risiko gagal bayar serta meningkatkan interpretabilitas model.

---

## 💡 Business Recommendations

- Mengintegrasikan model machine learning ke dalam proses credit scoring sebagai alat bantu pengambilan keputusan.
- Menggunakan probabilitas prediksi sebagai indikator tambahan untuk mengevaluasi pengajuan pinjaman dengan tingkat risiko tinggi.
- Memprioritaskan kualitas dan validasi data pada fitur-fitur yang memiliki pengaruh besar terhadap hasil prediksi.
- Melakukan retraining model secara berkala menggunakan data terbaru agar performa tetap optimal.
- Menyesuaikan strategi pemberian pinjaman, seperti limit kredit atau tenor, berdasarkan tingkat risiko yang diprediksi model.

---

## 📁 Repository Structure

```text
├── home_credit_default_risk_prediction.ipynb
├── submission_logreg.csv
├── submission_xgb.csv
└── README.md
```
