# Preprocessing Data Penjualan - Kelompok 5

Repositori ini berisi tahapan *data preprocessing* (pra-pemrosesan data) yang dilakukan pada dataset penjualan (`SCB_dataset_preprocessing_penjualan.csv`). Proses ini bertujuan untuk membersihkan, mentransformasikan, dan menyiapkan data agar siap digunakan untuk pemodelan analisis atau machine learning selanjutnya.

## Anggota Kelompok 5
1. Febry Aulia Utami Ahmad
2. Muhammad Nadhif Ihdar

---

## Alur Tahapan Preprocessing
Notebook disusun secara sistematis dengan format: **Penjelasan Singkat → Kode → Output → Interpretasi Hasil**. 

Tahapan utama yang dilakukan meliputi:
1. **Import Library:** Memuat pustaka Python seperti `numpy`, `pandas`, `matplotlib`, `seaborn`, dan `scikit-learn`.
2. **Memuat & Inspeksi Dataset:** Memeriksa dimensi data, tipe data, dan ringkasan statistik deskriptif (`info()` dan `describe()`).
3. **Penanganan Missing Value:** Mengidentifikasi persentase nilai kosong dan melakukan imputasi menggunakan modus (untuk kolom kategorikal) dan median (untuk kolom numerik).
4. **Penanganan Data Duplikat:** Mendeteksi dan menghapus baris data yang terduplikasi secara persis.
5. **Standarisasi Variabel Kategorikal:** Menyeragamkan penulisan nilai kategori yang tidak konsisten (seperti jenis kelamin, kota, kategori produk, dan metode pembayaran) menggunakan *dictionary mapping*.
6. **Koreksi Nilai Tidak Valid:** Membatasi (*clipping*) nilai di luar batas logis, seperti persentase diskon (0–100%) dan rating pelanggan (skala 1–5).
7. **Deteksi & Penanganan Outlier:** Mengidentifikasi pencilan pada data numerik menggunakan metode *Interquartile Range* (IQR) pada kolom harga satuan, total belanja, dan lama pengiriman.
8. **Penyimpanan Dataset Akhir:** Menyimpan hasil akhir data yang bersih (`df_cleaned`) ke dalam format file baru yang siap dianalisis.

---

## Kebutuhan Sistem (Dependencies)
Pastikan pustaka Python berikut telah terpasang di environment Anda:
* Python 3.x
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-Learn

## Cara Menjalankan
1. Pastikan file dataset `SCB_dataset_preprocessing_penjualan.csv` berada di direktori yang sama dengan notebook.
2. Jalankan sel-sel pada Jupyter Notebook secara berurutan dari atas ke bawah.
