# Home Credit Default Risk Prediction

## 📌 Project Type
Project-Based Internship – Home Credit Indonesia (Data Scientist)

## 📊 Overview

Project ini bertujuan untuk membangun model machine learning yang dapat memprediksi risiko gagal bayar (*credit default risk*) pada pengajuan pinjaman menggunakan dataset Home Credit. Model yang dihasilkan diharapkan dapat membantu proses *credit scoring* sehingga keputusan pemberian pinjaman menjadi lebih objektif, cepat, dan berbasis data.

Pipeline dikembangkan secara end-to-end mulai dari exploratory data analysis (EDA), data cleaning, feature engineering, preprocessing, penanganan *class imbalance*, hyperparameter tuning, evaluasi model, hingga prediksi probabilitas gagal bayar pada data testing.

---

## 🎯 Objectives

- Memahami karakteristik data dan distribusi target melalui exploratory data analysis.
- Melakukan data cleaning dan preprocessing untuk meningkatkan kualitas data.
- Mengembangkan fitur-fitur baru yang dapat meningkatkan performa model.
- Membangun dan membandingkan model Logistic Regression dan XGBoost.
- Melakukan hyperparameter tuning menggunakan GridSearchCV.
- Mengevaluasi performa model menggunakan ROC-AUC dan Log Loss.
- Mengidentifikasi fitur-fitur yang paling berpengaruh terhadap prediksi risiko gagal bayar.
- Menghasilkan probabilitas prediksi pada data testing.

---

## ⚙️ Machine Learning Pipeline

1. Data Understanding
2. Exploratory Data Analysis (EDA)
3. Data Cleaning
4. Feature Engineering
5. Train–Validation Split
6. Missing Value Imputation
7. Outlier Handling (Winsorization)
8. Feature Encoding and Scaling
9. Class Imbalance Handling
   - SMOTE (Logistic Regression)
   - `scale_pos_weight` (XGBoost)
10. Hyperparameter Tuning using GridSearchCV
11. Model Evaluation
12. Feature Importance Analysis
13. Prediction on Test Set

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

Dua algoritma yang digunakan dalam project ini adalah:

- **Logistic Regression**
- **XGBoost Classifier**

Hyperparameter tuning dilakukan menggunakan **GridSearchCV** dengan **Stratified 5-Fold Cross Validation**.

---

## 📈 Model Performance Benchmark

### Best Hyperparameters

| Model | Best Parameters |
|---------|----------------|
| Logistic Regression | `C = 0.01`, `penalty = l1`, `solver = liblinear`, `max_iter = 300` |
| XGBoost | `n_estimators = 200`, `max_depth = 5`, `learning_rate = 0.1`, `scale_pos_weight = 11` |

### Validation Set Performance

| Algorithm | ROC-AUC | Log Loss |
|------------|--------:|---------:|
| Logistic Regression | **0.7447** | **0.5836** |
| XGBoost | **0.7680** | **0.5358** |

Berdasarkan hasil evaluasi pada validation set, **XGBoost** dipilih sebagai model terbaik karena menghasilkan **ROC-AUC yang lebih tinggi** dan **Log Loss yang lebih rendah** dibandingkan Logistic Regression. Oleh karena itu, model XGBoost digunakan untuk menghasilkan prediksi pada data testing.

---

## 📤 Prediction on Test Set

Model XGBoost digunakan untuk memprediksi probabilitas gagal bayar pada **48.744** data aplikasi pinjaman yang tidak memiliki label target.

Contoh hasil prediksi:

| SK_ID_CURR | Predicted Probability (`TARGET`) |
|------------|---------------------------------:|
| 100001 | 0.262007 |
| 100005 | 0.523379 |
| 100013 | 0.116791 |
| 100028 | 0.317475 |
| 100038 | 0.611128 |

Output prediksi disimpan dalam file:

- `submission_xgb.csv`

---

## 🔍 Top 10 Feature Importance (XGBoost)

Sepuluh fitur dengan kontribusi terbesar berdasarkan model XGBoost adalah:

1. `EXT_SOURCE_MEAN`
2. `NAME_EDUCATION_TYPE`
3. `CODE_GENDER`
4. `FLAG_DOCUMENT_3`
5. `FLAG_OWN_CAR`
6. `GOODS_CREDIT_RATIO`
7. `EXT_SOURCE_MAX`
8. `LOAN_DURATION_MONTHS`
9. `NAME_CONTRACT_TYPE`
10. `FLAG_EMP_PHONE`

Fitur-fitur tersebut memberikan kontribusi terbesar dalam membantu model membedakan pemohon dengan risiko gagal bayar yang lebih tinggi maupun lebih rendah.

---

## 💡 Business Recommendations

- Mengintegrasikan model XGBoost ke dalam proses credit scoring sebagai alat bantu pengambilan keputusan.
- Menggunakan probabilitas prediksi sebagai indikator tambahan dalam mengevaluasi pengajuan pinjaman berisiko tinggi.
- Memprioritaskan kualitas data pada fitur-fitur yang memiliki pengaruh besar terhadap hasil prediksi, terutama variabel yang berasal dari sumber data eksternal (*EXT_SOURCE*).
- Melakukan retraining model secara berkala menggunakan data terbaru agar performa prediksi tetap optimal.
- Menyesuaikan strategi pemberian pinjaman, seperti limit kredit, tenor, atau kebijakan mitigasi risiko lainnya, berdasarkan tingkat risiko yang diprediksi model.

---
