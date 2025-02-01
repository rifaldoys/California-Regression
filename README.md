# README: Analisis dan Prediksi Harga Rumah di California

## Deskripsi
Repositori ini berisi kode Python untuk melakukan analisis eksploratif dan prediksi harga rumah di California menggunakan dataset `fetch_california_housing` dari `sklearn.datasets`. Proyek ini mencakup berbagai teknik pemrosesan data, eksplorasi data, pemodelan regresi, dan evaluasi model untuk memahami faktor-faktor yang mempengaruhi harga rumah di wilayah tersebut.

## Struktur Kode
1. **Import Library**
   - Menggunakan pustaka seperti `numpy`, `pandas`, `matplotlib`, `seaborn`, dan `sklearn` untuk manipulasi data dan pemodelan.
   - Menggunakan `geopandas` dan `contextily` untuk analisis geospasial.

2. **Memuat Dataset**
   - Menggunakan `fetch_california_housing()` untuk mendapatkan data.
   - Memisahkan fitur (`X`) dan target (`y`).

3. **Eksplorasi Data (EDA)**
   - Menampilkan struktur data, nilai yang hilang, dan statistik deskriptif.
   - Menganalisis distribusi harga rumah menggunakan histogram.
   - Visualisasi geospasial untuk menunjukkan penyebaran harga rumah berdasarkan lokasi.
   - Korelasi antar fitur menggunakan heatmap dan cluster map.
   - Visualisasi hubungan antar fitur dengan pairplot.

4. **Preprocessing Data**
   - Membagi data menjadi train dan test dengan `train_test_split()`.
   - Menggunakan `StandardScaler` dan `PolynomialFeatures` dalam pipeline preprocessing.

5. **Pemodelan**
   - Menggunakan model regresi:
     - **Linear Regression**
     - **Ridge Regression**
     - **Lasso Regression**
     - **ElasticNet Regression**
   - Hyperparameter tuning dengan `RandomizedSearchCV`.

6. **Evaluasi Model**
   - Menghitung metrik evaluasi seperti:
     - **Mean Absolute Error (MAE)**
     - **Root Mean Squared Error (RMSE)**
     - **R-squared (R²)**
   - Membandingkan hasil model dalam bentuk tabel.
   - Visualisasi prediksi vs aktual dalam bentuk scatter plot.
   - Analisis residual model.
   - Menampilkan feature importance untuk model dengan regularisasi.
   - Partial Dependence Plot untuk memahami pengaruh fitur terhadap target.

7. **Interpretasi Model**
   - Cross-validation dengan 10-fold CV untuk mendapatkan RMSE yang lebih stabil.
   - Menampilkan persamaan model terbaik berdasarkan hasil regresi ElasticNet.

## Cara Menjalankan
1. Pastikan Anda memiliki Python 3.x dan pustaka yang diperlukan.
2. Install pustaka tambahan dengan menjalankan:
   ```sh
   pip install numpy pandas matplotlib seaborn scikit-learn geopandas contextily
   ```
3. Jalankan skrip Python secara berurutan untuk melakukan analisis dan pemodelan.

## Hasil dan Kesimpulan
- Model **Ridge Regression** memiliki performa terbaik dengan RMSE terendah.
- Fitur **MedInc (Median Income)** memiliki pengaruh terbesar terhadap harga rumah.
- Korelasi antar fitur membantu dalam memahami hubungan antar variabel.
- Penggunaan **Partial Dependence Plot** membantu interpretasi model.

## Pengembangan Selanjutnya
- Menggunakan model non-linear seperti **Random Forest** atau **Gradient Boosting**.
- Menambahkan fitur eksternal seperti informasi ekonomi atau sosial.
- Menggunakan deep learning untuk meningkatkan akurasi prediksi.

---
Dokumen ini dibuat untuk memberikan pemahaman yang jelas tentang proyek dan langkah-langkah yang dilakukan dalam analisis harga rumah di California.

