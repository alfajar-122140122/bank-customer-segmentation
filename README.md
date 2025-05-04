# Customer Segmentation with Divisive Clustering

Project ini bertujuan untuk melakukan segmentasi pelanggan bank menggunakan metode **Divisive Clustering** (hierarchical clustering top-down) pada data transaksi nasabah. Analisis dilakukan dengan Python dan Jupyter Notebook.

## Identitas
Kelompok 3 - Pembelajaran Mesin 

## Struktur Proyek

- `customer_segementation.ipynb` — Notebook utama berisi seluruh workflow analisis dan clustering.
- `data/bank_transactions.csv` — Dataset transaksi pelanggan (tidak diupload ke GitHub).
- `requirements.txt` — Daftar library Python yang digunakan.
- `.gitignore` — Mengabaikan folder venv dan file sementara.

## Alur Analisis

1. **Import Library**  
   Menggunakan pandas, numpy, matplotlib, scikit-learn, scipy, dll.

2. **Load Dataset**  
   Membaca data transaksi pelanggan dari file CSV.

3. **Preprocessing**  
   - Menghapus data duplikat dan missing value.
   - Mengubah tanggal lahir (`CustomerDOB`) menjadi umur (`Age`).
   - Memilih fitur relevan: `Age`, `CustAccountBalance`, `TransactionAmount (INR)`.

4. **Normalisasi Data**  
   Menstandarisasi fitur agar skala seragam.

5. **Divisive Clustering**  
   - Menggunakan hierarchical clustering (`ward linkage`) dan visualisasi dendrogram.
   - Menentukan jumlah cluster optimal dengan silhouette score.

6. **Evaluasi & Visualisasi**  
   - Menghitung silhouette score dan Davies-Bouldin Index.
   - Membandingkan hasil dengan KMeans.
   - Visualisasi hasil clustering dalam 3D.

## Cara Menjalankan

1. **Clone repository ini**
2. **Buat virtual environment dan install requirements**
   ```bash
   python -m venv venv
   venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. **Jalankan notebook di Jupyter**
   ```bash
   jupyter notebook
   ```
4. **Buka dan jalankan `customer_segementation.ipynb`**

## Catatan

- Dataset tidak diupload ke GitHub, silakan letakkan file `bank_transactions.csv` di folder `data/`.
- Folder `venv` tidak perlu diupload, sudah diabaikan oleh `.gitignore`.

## Lisensi

Proyek ini untuk keperluan pembelajaran dan tugas akademik.
