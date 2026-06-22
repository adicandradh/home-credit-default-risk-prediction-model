# Home Credit Default Risk Prediction

## 📌 Project Type
Project-Based Internship – Home Credit Indonesia (Data Scientist)

## 📊 Overview

Project ini bertujuan untuk membangun model machine learning yang dapat memprediksi risiko gagal bayar (*credit default risk*) pada pengajuan pinjaman menggunakan dataset Home Credit. Model yang dihasilkan diharapkan dapat membantu proses *credit scoring* sehingga keputusan pemberian pinjaman menjadi lebih objektif, cepat, dan berbasis data.

Pipeline dikembangkan secara end-to-end mulai dari exploratory data analysis (EDA), data cleaning, feature engineering, preprocessing, penanganan *class imbalance*, hyperparameter tuning, evaluasi model, hingga prediksi probabilitas gagal bayar pada **data testing**.

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
13. Prediction on Test Data

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

Project ini membandingkan dua algoritma klasifikasi, yaitu:

- **Logistic Regression**
- **XGBoost Classifier**

Hyperparameter tuning dilakukan menggunakan **GridSearchCV** dengan **Stratified 5-Fold Cross Validation** untuk memperoleh kombinasi parameter terbaik pada masing-masing model.

---

## 📈 Model Performance

### Best Hyperparameters

| Model | Best Parameters |
|---------|----------------|
| Logistic Regression | `C = 0.01`, `penalty = l1`, `solver = liblinear`, `max_iter = 300` |
| XGBoost | `n_estimators = 200`, `max_depth = 5`, `learning_rate = 0.1`, `scale_pos_weight = 11` |

### Validation Data Performance

| Algorithm | ROC-AUC | Log Loss |
|------------|--------:|---------:|
| Logistic Regression | **0.7447** | **0.5836** |
| XGBoost | **0.7680** | **0.5358** |

Berdasarkan hasil evaluasi pada **validation data**, **XGBoost** dipilih sebagai model terbaik karena menghasilkan **ROC-AUC** yang lebih tinggi dan **Log Loss** yang lebih rendah dibandingkan Logistic Regression. Oleh karena itu, model XGBoost digunakan untuk menghasilkan prediksi pada **test data**.

---

## 📤 Prediction on Test Data

Model XGBoost digunakan untuk memprediksi probabilitas gagal bayar pada **48.744 data testing** yang tidak memiliki label target.

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

Berdasarkan hasil pelatihan model **XGBoost**, sepuluh fitur berikut memberikan kontribusi terbesar dalam memprediksi risiko gagal bayar pada **data training**:

| Rank | Feature | Description |
|------|---------|-------------|
| 1 | `EXT_SOURCE_MEAN` | Rata-rata skor dari `EXT_SOURCE_1`, `EXT_SOURCE_2`, dan `EXT_SOURCE_3` yang merepresentasikan profil risiko calon nasabah. |
| 2 | `NAME_EDUCATION_TYPE` | Tingkat pendidikan tertinggi yang dimiliki oleh calon nasabah. |
| 3 | `CODE_GENDER` | Jenis kelamin calon nasabah. |
| 4 | `FLAG_DOCUMENT_3` | Indikator apakah calon nasabah menyerahkan dokumen pendukung tertentu saat pengajuan pinjaman. |
| 5 | `FLAG_OWN_CAR` | Indikator kepemilikan kendaraan oleh calon nasabah. |
| 6 | `GOODS_CREDIT_RATIO` | Rasio antara nilai barang yang dibiayai (`AMT_GOODS_PRICE`) dengan jumlah kredit (`AMT_CREDIT`). |
| 7 | `EXT_SOURCE_MAX` | Nilai maksimum dari `EXT_SOURCE_1`, `EXT_SOURCE_2`, dan `EXT_SOURCE_3`. |
| 8 | `LOAN_DURATION_MONTHS` | Estimasi durasi pinjaman dalam bulan berdasarkan jumlah kredit dan nilai anuitas. |
| 9 | `NAME_CONTRACT_TYPE` | Jenis kontrak pinjaman yang diajukan oleh nasabah. |
| 10 | `FLAG_EMP_PHONE` | Indikator apakah calon nasabah memberikan nomor telepon kantor atau pekerjaan. |

Hasil tersebut menunjukkan bahwa informasi dari sumber data eksternal (*EXT_SOURCE*), karakteristik demografis, serta beberapa fitur hasil *feature engineering* memberikan kontribusi yang signifikan dalam membedakan pemohon dengan risiko gagal bayar tinggi maupun rendah.

---

## 💡 Business Recommendations

- Mengintegrasikan model XGBoost ke dalam proses *credit scoring* sebagai alat bantu pengambilan keputusan pemberian pinjaman.
- Menggunakan probabilitas prediksi sebagai indikator tambahan dalam mengevaluasi pengajuan pinjaman yang memiliki risiko gagal bayar tinggi.
- Memprioritaskan kualitas dan validasi data pada fitur-fitur yang memiliki pengaruh besar terhadap hasil prediksi, terutama variabel yang berasal dari sumber data eksternal (*EXT_SOURCE*).
- Melakukan *retraining* model secara berkala menggunakan data terbaru agar performa prediksi tetap optimal.
- Menyesuaikan strategi pemberian pinjaman, seperti limit kredit, tenor, atau kebijakan mitigasi risiko lainnya, berdasarkan tingkat risiko yang diprediksi model.

---
