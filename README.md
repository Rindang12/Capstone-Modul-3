# 🏠 California Housing Price Prediction

Proyek ini bertujuan untuk memprediksi **median house value** di California menggunakan berbagai algoritma **regresi** seperti Linear Regression, Lasso, Ridge, Random Forest, dan XGBoost.

---

## 📌 Project Overview

Dataset yang digunakan berasal dari **California Housing Dataset**, berisi informasi seperti:
- Total rooms, bedrooms, population, households
- Median income
- Lokasi geografis (longitude & latitude)
- Ocean proximity

Tujuan utama:  
➡️ **Memprediksi harga rata-rata rumah (`median_house_value`) berdasarkan karakteristik wilayah.**

---

## 📊 Dataset

- Sumber: California Housing Dataset (`sklearn.datasets.fetch_california_housing`)
- Ukuran: 20.000+ baris data
- Target: `median_house_value`
- Fitur utama:
  - `median_income`
  - `total_rooms`, `total_bedrooms`
  - `population`, `households`
  - `latitude`, `longitude`
  - `ocean_proximity` (one-hot encoded)

---

## 🔧 Preprocessing

- One-hot encoding untuk fitur kategorikal (`ocean_proximity`)
- Penanganan missing values & outliers
- Normalisasi data numerik (jika diperlukan)
- Pembagian data: 80% training, 20% testing

---

## ⚙️ Modeling

Model yang digunakan:
- 📈 Linear Regression
- 📉 Lasso Regression
- 🔧 Ridge Regression
- 🌳 Random Forest Regressor
- 🚀 XGBoost Regressor

Metode evaluasi:
- R² Score dan Adjusted R²
- MAE (Mean Absolute Error)
- MSE & RMSE
- MAPE & MSPE
- MSLE (jika applicable)

---

## 🧪 Evaluation Result

| Model              | R²     | Adjusted R² | MAE     | MSE         | RMSE    | MAPE    | MSPE   | MSLE   |
|--------------------|--------|-------------|---------|-------------|---------|---------|--------|--------|
| Linear Regression  | 0.5531 | 0.5523      | 47,436  | 3.97e+09    | 63,010  | 0.308   | 0.196  | -      |
| Lasso Regression   | 0.5531 | 0.5524      | 47,435  | 3.97e+09    | 63,010  | 0.308   | 0.196  | -      |
| Ridge Regression   | 0.5531 | 0.5523      | 47,436  | 3.97e+09    | 63,010  | 0.308   | 0.196  | -      |
| Random Forest      | 0.7561 | 0.7556      | 31,346  | 2.17e+09    | 46,552  | 0.183   | 0.094  | 0.057  |
| XGBoost            | 0.7755 | 0.7751      | 30,017  | 1.99e+09    | 44,656  | 0.176   | 0.090  | 0.057  |

✅ **XGBoost** menghasilkan performa terbaik dengan R² tertinggi dan error terkecil.

---

## 📌 Why Regression?

- Target (median house value) adalah **numerik & kontinu**
- Tujuan proyek adalah **prediksi nilai**, bukan klasifikasi
- Terdapat korelasi fungsional antara fitur dan target

---
