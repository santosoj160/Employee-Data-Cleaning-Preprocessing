#  Comprehensive Employee Data Cleaning & Preprocessing Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-150458.svg)
![NumPy](https://img.shields.io/badge/NumPy-Data%20Manipulation-013243.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-Data%20Visualization-3776AB.svg)
![Google Colab](https://img.shields.io/badge/Environment-Google%20Colab-F9AB00.svg)

---

##  1. Latar Belakang & Tujuan Proyek

Proyek ini berfokus pada **Data Cleaning & Preprocessing** untuk dataset karyawan (*Employee Dataset*). Data mentah (*raw data*) yang dikumpulkan dari sistem HR sering kali mengandung kebocoran data, pencatatan ganda, inkonsistensi input manual, serta nilai-nilai ekstrem yang tidak rasional. Jika langsung digunakan untuk analisis atau algoritma *Machine Learning*, data berkualitas rendah ini akan menghasilkan keputusan bisnis yang bias.

###  Tujuan Utama Proyek:
1. **Pembersihan Struktur Data:** Mengidentifikasi dan menghapus data duplikat serta menstandardisasi format teks/kategorikal.
2. **Deteksi & Handling Outlier:** Menggunakan pendekatan statistik rasional tanpa menghilangkan informasi sebaran data alami.
3. **Imputasi Data Kosong:** Mengatasi *missing values* berdasarkan sifat dan distribusi tiap fitur.
4. **Transformasi Fitur (Encoding):** Mengubah data tekstual/kategorikal menjadi bentuk biner dan matriks numerik yang siap diproses oleh model.


##  2. Struktur Repositori & File

```text
.
├── assignment_data_cleaning_joko.ipynb   # Notebook utama Google Colab (Kode & Visualisasi)
├── Presentation_Data_Cleaning.pdf        # Slide Presentasi Canva (Laporan Eksekutif)
├── employee_data.csv                     # Raw Dataset Awal
└── README.md                             # Dokumentasi Teknis Terperinci 
```
---

##  3. Kamus Data & Variabel Awal

Dataset awal berisi **1.248 baris dan 14 kolom** (kombinasi variabel kategorikal dan numerik seperti `employee_id`, `department`, `education_level`, `age`, `monthly_salary`, dll).

---

##  4. Metodologi & Preprocessing

* **Task 1 — EDA & Text Standardization:** Menghapus 43 data duplikat (`df.drop_duplicates()`) serta merapikan format teks pada kolom `department` (`it` -> `IT`) dan `city` (`jakarta` -> `Jakarta`).
* **Task 2 — Outlier Handling:** Mendeteksi 32 data ekstrem di kolom `age`, `monthly_salary`, `training_hours`, dan `overtime_hours` menggunakan batas IQR, lalu dipangkas rasional (*Capping / Winsorization*).
* **Task 3 — Missing Value Handling:** Mengisi data hilang (~8%) menggunakan **Modus** untuk `education_level` dan **Median** untuk kolom numerik (`monthly_salary`, `satisfaction_score`, `training_hours`).
* **Task 4 — Feature Encoding:** Mengubah data ordinal (`performance_category`) dengan **Label Encoding**, serta data nominal (`department` dan `work_mode`) dengan **One-Hot Encoding** (`drop_first=True`).

---

##  5. Summary (Before vs After)

* **Total Baris:** Dari 1.248 baris -> **1.205 baris unik** (bersih dari duplikat).
* **Missing Values:** Dari ~8% data kosong -> **0%** (terisi sempurna).
* **Outliers:** Dari 32 data ekstrem -> **Dipangkas rasional** (*Capped*).
* **Format Data:** Dari campuran teks & angka -> **20 kolom full numerik** (siap untuk ML).

---

## 🔗 Project Links & Assets

* 💻 **Google Colab Notebook:** [Data_Cleaning_joko](https://colab.research.google.com/drive/1aSv2ClqT0YdsMzKsPytpSzk_4YaBxTL7?usp=sharing)
* 🎨 **Canva Presentation Deck:** [Interactive Presentation Slide](https://canva.link/rj0tsqak1w9r7i5)
* 💼 **Author / Connect with me:** [Joko Santoso](https://www.linkedin.com/in/joko-santoso-484769144)
