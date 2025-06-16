# Prediksi Harga Rumah Berdasarkan Data Statistik Area

Proyek ini bertujuan untuk memprediksi harga rumah berdasarkan data statistik area menggunakan model regresi linier. Dataset yang digunakan berisi informasi tentang pendapatan rata-rata area, usia rumah, jumlah kamar, jumlah kamar tidur, populasi area, harga rumah, dan alamat.

## Struktur Proyek

```
readme.md
data/
    dataset.csv
src/
    index.ipynb
```

- **`data/dataset.csv`**: Dataset yang digunakan untuk analisis dan pelatihan model.
- **`src/index.ipynb`**: Notebook Jupyter yang berisi kode untuk analisis data, visualisasi, pelatihan model, dan evaluasi.

## Fitur Proyek

1. **Analisis Data**:
   - Menampilkan informasi dataset (`df.info()`).
   - Statistik deskriptif (`df.describe()`).
   - Visualisasi distribusi fitur dan hubungan antar fitur.

2. **Preprocessing Data**:
   - Menghapus nilai kosong (`df.dropna()`).
   - Memisahkan fitur dan target untuk pelatihan model.

3. **Visualisasi**:
   - Pairplot untuk melihat hubungan antar fitur.
   - Heatmap untuk melihat korelasi antar fitur.
   - Histogram distribusi harga rumah.

4. **Modeling**:
   - Menggunakan regresi linier untuk memprediksi harga rumah.
   - Evaluasi model menggunakan metrik seperti MAE, MSE, RMSE, dan R².

5. **Prediksi**:
   - Prediksi harga rumah berdasarkan data baru.

## Cara Menjalankan Proyek

1. **Persiapan Lingkungan**:
   - Pastikan Python dan Jupyter Notebook telah terinstal.
   - Instal pustaka yang diperlukan:
     ```bash
     pip install pandas numpy seaborn matplotlib scikit-learn
     ```

2. **Menjalankan Notebook**:
   - Buka file `src/index.ipynb` menggunakan Jupyter Notebook.
   - Jalankan setiap sel untuk melakukan analisis, pelatihan model, dan prediksi.

## Dataset

Dataset berisi 5000 baris data dengan kolom berikut:
- `Avg. Area Income`: Pendapatan rata-rata area.
- `Avg. Area House Age`: Usia rata-rata rumah di area.
- `Avg. Area Number of Rooms`: Jumlah rata-rata kamar di rumah.
- `Avg. Area Number of Bedrooms`: Jumlah rata-rata kamar tidur di rumah.
- `Area Population`: Populasi area.
- `Price`: Harga rumah.
- `Address`: Alamat rumah.

## Hasil Model

Model regresi linier menghasilkan metrik evaluasi berikut:
- **Mean Absolute Error (MAE)**: Nilai rata-rata kesalahan absolut.
- **Mean Squared Error (MSE)**: Nilai rata-rata kesalahan kuadrat.
- **Root Mean Squared Error (RMSE)**: Akar dari MSE.
- **R² Score**: Koefisien determinasi untuk mengukur performa model.

## Prediksi Data Baru

Contoh prediksi harga rumah berdasarkan data baru:
```python
new_data = pd.DataFrame({
    'Avg. Area Income': [74568.64],
    'Avg. Area House Age': [5.182],
    'Avg. Area Number of Rooms': [7.62],
    'Avg. Area Number of Bedrooms': [4.09],
    'Area Population': [25045.34],
})

new_predictions = lm.predict(new_data)
print(f"Predicted Price for new data: {new_predictions[0]:.0f}")
```

## Lisensi

Proyek ini dilisensikan di bawah