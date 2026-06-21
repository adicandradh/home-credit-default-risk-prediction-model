# 🏦 Home Credit Default Risk Prediction

## 📌 Project Type
Project-Based Internship – Home Credit Indonesia (Data Scientist)

## 📊 Overview

Project ini merupakan implementasi machine learning untuk memprediksi risiko gagal bayar (credit default risk) pada pengajuan pinjaman menggunakan dataset Home Credit.

Model dikembangkan untuk membantu proses credit scoring sehingga keputusan pemberian pinjaman dapat dilakukan secara lebih akurat dan berbasis data. Dengan memanfaatkan informasi historis calon nasabah, model diharapkan mampu membedakan pemohon dengan risiko gagal bayar rendah maupun tinggi, sehingga dapat mendukung pengelolaan risiko kredit yang lebih efektif.

Project ini mencakup proses end-to-end mulai dari exploratory data analysis (EDA), data cleaning, feature engineering, data preprocessing, model training, hyperparameter tuning, model evaluation, hingga prediksi pada data testing.

## 🎯 Objectives

- Melakukan exploratory data analysis (EDA) untuk memahami karakteristik dataset.
- Membersihkan dan mempersiapkan data sebelum proses pemodelan.
- Mengembangkan fitur-fitur baru yang dapat meningkatkan performa model.
- Membangun dan membandingkan dua model machine learning, yaitu Logistic Regression dan XGBoost.
- Melakukan hyperparameter tuning untuk memperoleh konfigurasi model terbaik.
- Mengevaluasi performa model menggunakan ROC-AUC dan Log Loss.
- Mengidentifikasi fitur-fitur yang paling berpengaruh terhadap prediksi risiko gagal bayar.
- Menghasilkan prediksi probabilitas default pada data testing.

## ⚙️ Machine Learning Pipeline

1. Data Understanding
2. Exploratory Data Analysis (EDA)
3. Data Cleaning
4. Feature Engineering
5. Train-Validation Split
6. Missing Value Handling
7. Outlier Handling (Winsorization)
8. Encoding & Feature Scaling
9. Model Training
10. Hyperparameter Tuning
11. Model Evaluation
12. Prediction on Test Dataset
13. Feature Importance Analysis

## 🔧 Data Preprocessing

Tahapan preprocessing yang diterapkan meliputi:

- Penanganan missing values menggunakan imputasi.
- Penanganan nilai anomali pada beberapa variabel.
- Winsorization untuk mengurangi pengaruh outlier.
- Feature engineering berbasis karakteristik finansial dan profil nasabah.
- Encoding variabel kategorikal menggunakan `OrdinalEncoder`.
- Standardisasi fitur numerik menggunakan `StandardScaler`.
- Penanganan class imbalance menggunakan `SMOTE`.

## 🤖 Machine Learning Models

Model yang digunakan pada project ini:

- Logistic Regression
- XGBoost Classifier

Hyperparameter tuning dilakukan menggunakan **RandomizedSearchCV** dengan **Stratified 5-Fold Cross Validation**.

## 📈 Model Performance Benchmark

Evaluasi dilakukan menggunakan **Stratified 5-Fold Cross Validation**.

| Algorithm | Mean ROC-AUC | Mean Log Loss |
|------------|-------------:|--------------:|
| Logistic Regression | `<<ISI SETELAH RUN>>` | `<<ISI SETELAH RUN>>` |
| XGBoost | `<<ISI SETELAH RUN>>` | `<<ISI SETELAH RUN>>` |

### Validation Set Performance

| Algorithm | ROC-AUC | Log Loss |
|------------|--------:|---------:|
| Logistic Regression | `<<ISI SETELAH RUN>>` | `<<ISI SETELAH RUN>>` |
| XGBoost | `<<ISI SETELAH RUN>>` | `<<ISI SETELAH RUN>>` |

> **Selected Model:** `<<ISI SETELAH RUN (misal: XGBoost)>>` dipilih sebagai model terbaik berdasarkan hasil evaluasi ROC-AUC dan Log Loss.

## 🔍 Top Feature Importance

Berdasarkan model terbaik, enam fitur yang paling berpengaruh terhadap prediksi risiko gagal bayar adalah:

| Rank | Feature |
|------|---------|
| 1 | `<<ISI SETELAH RUN>>` |
| 2 | `<<ISI SETELAH RUN>>` |
| 3 | `<<ISI SETELAH RUN>>` |
| 4 | `<<ISI SETELAH RUN>>` |
| 5 | `<<ISI SETELAH RUN>>` |
| 6 | `<<ISI SETELAH RUN>>` |

## 💡 Business Recommendations

- Mengintegrasikan model machine learning sebagai alat bantu dalam proses credit scoring untuk meningkatkan konsistensi pengambilan keputusan.
- Memanfaatkan probabilitas prediksi sebagai indikator tambahan dalam mengevaluasi pengajuan pinjaman berisiko tinggi.
- Memprioritaskan validasi dan kualitas data pada fitur-fitur yang memiliki kontribusi besar terhadap performa model.
- Melakukan retraining model secara berkala menggunakan data terbaru agar performa prediksi tetap optimal.
- Menyesuaikan strategi pemberian pinjaman, seperti limit kredit atau tenor, berdasarkan tingkat risiko yang diprediksi oleh model.

## 🛠️ Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- XGBoost
