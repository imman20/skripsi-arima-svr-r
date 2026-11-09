# Kode R Skripsi: ARIMA vs SVR untuk Prediksi Kurs Rupiah

Kode R asli yang saya tulis untuk skripsi S1 Statistika Universitas Airlangga (2024):
**"Perbandingan Model Autoregressive Integrated Moving Average (ARIMA) dan Support Vector Regression (SVR) untuk Prediksi Nilai Tukar Rupiah terhadap Dolar AS."**

Repositori ini sengaja saya biarkan apa adanya sebagai arsip pekerjaan skripsi. Versi Python yang lebih rapi, dapat direproduksi, dan dikembangkan (uji Diebold-Mariano, Value at Risk, aplikasi Streamlit) ada di **[forecast-kurs-rupiah-arima-svr](https://github.com/imman20/forecast-kurs-rupiah-arima-svr)**.

## Ringkasan

| Aspek | Keterangan |
|---|---|
| Data | Kurs USD/IDR mingguan, Oktober 2021 – Oktober 2023 (105 observasi) |
| Pembagian | 84 minggu training, 21 minggu testing |
| ARIMA | Uji linieritas Terasvirta, transformasi Box-Cox, differencing, identifikasi ACF/PACF, uji signifikansi parameter dan diagnostik residual |
| SVR | Kernel linear, polinomial, dan RBF dengan tuning hyperparameter (`e1071`) |
| Evaluasi | MAPE pada data testing |
| Hasil | ARIMA (0,2,1) MAPE 2,49 %; SVR kernel RBF MAPE 0,54 % |

## Isi folder

| File | Isi |
|---|---|
| `Program ARIMA SVR.R` | Alur lengkap: eksplorasi data, pembagian training/testing, Box-Cox, pemodelan ARIMA, pemodelan SVR, dan evaluasi |
| `ARIMA SVR.R` | Versi kerja sebelumnya dari skrip yang sama |

## Cara menjalankan

1. Siapkan file data `week2a.xlsx` (kolom `nilai` berisi kurs mingguan) di satu folder.
2. Buka skrip di RStudio, lalu atur working directory ke folder tersebut (baris `setwd` sudah saya ganti menjadi komentar).
3. Pasang paket yang dipakai: `readxl`, `e1071`, `MLmetrics`, `tseries`, `forecast`, `lmtest`, `zoo`, `openxlsx`.
4. Jalankan skrip dari atas ke bawah.

## Kontak

Immantaka Juniarsa · immantakajuniarsa30@gmail.com · [Portofolio](https://imman20.github.io/)
