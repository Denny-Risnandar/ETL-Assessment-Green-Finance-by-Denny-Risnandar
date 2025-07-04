# ETL-Assessment-Green-Finance-by-Denny-Risnandar
Ditujukan untuk Assesment ETL Kelompok
---
| Nama               | No Absen       | Kelompok |
|--------------------|----------------|----------|
|Alif Nur Rahman     | 10.028.DB2025  | III      |
|Asfa Asfialana      | 10.037.DB2025  | III      |
|Denny Risnandar     | 09.030.DB2025  | III      |
|Ihsan Ahsanul Amala | 09.044.DB2025  | III      |

---

## Green Finance Data Analysis

## 1. Pendahuluan

### 1.1  Latar Belakang
Apa itu Green Finance? Simpelnya, Green Finance adalah kegiatan keuangan apapun yang dilakukan untuk mendukung kelestarian lingkungan yang lebih baik. Misalnya, investasi di sektor energi terbarukan, transportasi ramah lingkungan, atau pertanian organik. Green Finance juga bisa berbentuk instrumen keuangan yang memperhatikan dampak lingkungan, seperti obligasi hijau (investasi yg dalam kegiatan usahanya berhubungan dengan lingkungan), bank hijau (Lembaga keuangan yang menggunakan Teknik pembiayaan inovatif an alat pengembangan pasar melalui kemitraan dengan sector swasta untuk mempercepat penerapan teknologi energi ramah lingkungan), atau pasar karbon mekanisme yang memungkinkan terjadinya negosiasi dan pertukaran hak emisi gas rumah kaca.

Kenapa Green Finance itu penting? Karena menurut World Bank, Green Finance bisa membantu kita mencapai tujuan ekonomi, sekaligus peduli sama kondisi sosial dan lingkungan. Kalau mau lebih spesifik lagi nih, Green Finance bisa meningkatkan ketahanan energi dan mengurangi emisi gas rumah kaca. Udah tau kan kalau gas rumah kaca itu salah satu penyebab perubahan iklim? Green Finance bisa memberikan manfaat ekonomi dan lingkungan bagi semua pihak, baik individu maupun perusahaan dengan memberikan akses ke barang dan jasa yang ramah lingkungan dan mendorong pertumbuhan yang lebih inklusif.

### 1.2. 📝 Rumusan Masalah yang akan dianalisis

Rumusan masalah yang akan kita lakukan analisis dalam proyek analisis green finance kali ini adalah :

1. Bagaimana mengidentifikasi proyek **PLTS** yang memiliki efisiensi pengurangan CO₂ tertinggi per satuan **juta rupiah investasi**?
2. Berapa rata-rata pengurangan emisi CO₂ dari seluruh proyek **PLTM** untuk menilai dampak lingkungan kolektifnya?
3. Bagaimana merancang alat yang dapat menampilkan **status lahan dan tingkat konflik sosial** berdasarkan **Project_ID**?
4. Proyek mana saja yang memiliki **daya tarik investasi tinggi** namun dengan **tingkat konflik sosial rendah** sehingga dapat meminimalkan risiko?
5. Bagaimana menghitung **total investasi** untuk proyek-proyek yang memiliki **efisiensi lokasi tinggi**?
6. Bagaimana membangun **alat komputasi efisiensi CO₂** yang dapat digunakan kembali dan memiliki kemampuan **penanganan kesalahan** (error handling)?
7. Bagaimana menghitung **rata-rata keluaran energi** dari proyek-proyek terpilih, dengan memperhitungkan **data yang hilang** (missing data)?
8. Bagaimana memprediksi tingkat **daya tarik investasi** ("High", "Medium", "Low") untuk proyek-proyek baru berdasarkan variabel seperti **GDP_Growth**, **CO₂_Reduction**, dan **Investment_Cost**?


### 1.3. 🎯 Tujuan Analisis

Analisis green finance yang dilakukan bertujuan :

1. Mengukur efisiensi pengurangan CO₂ dari proyek PLTS per satuan biaya investasi.
2. Menentukan dampak lingkungan kolektif dari proyek PLTM melalui penghitungan rata-rata pengurangan emisi CO₂.
3. Mengembangkan alat input berbasis **Project_ID** untuk mengecek **status lahan** dan **tingkat konflik sosial**.
4. Mengidentifikasi proyek yang menarik secara finansial dan rendah konflik sosial sebagai prioritas investasi.
5. Menghitung total investasi pada proyek-proyek yang memiliki **lokasi strategis** dan efisien.
6. Membangun alat komputasi efisiensi CO₂ yang **tangguh**, **dapat digunakan ulang**, dan **andal**.
7. Menganalisis rata-rata **energy output** meskipun terdapat data tidak lengkap.
8. Membangun model prediktif klasifikasi daya tarik investasi berdasarkan variabel-variabel ekonomi dan lingkungan.
9. Sebagai syarat menyelesaikan Asessment Task Eco Techno Leader

### 1.4. Manfaat Analisis

Diharapkan hasil analisis green finance ini dapat memberi manfaat, seperti :

- Memberikan **rekomendasi berbasis data** untuk mendukung kebijakan investasi energi terbarukan pemerintah.
- Menyediakan **alat bantu analisis praktis** untuk stakeholder dan pengambil kebijakan.
- Mempermudah proses seleksi dan pemantauan proyek yang **berdampak besar dan rendah risiko**.
- Mendorong perencanaan proyek yang lebih **strategis, efisien, dan berkelanjutan**.
- Meningkatkan efisiensi penggunaan anggaran negara untuk mendukung **transisi energi hijau**.

## 2. Kajian Pustaka / Landasan Teori

### 2.1 Pengertian Green Finance

Green Finance adalah kegiatan keuangan apapun yang dilakukan untuk mendukung kelestarian lingkungan yang lebih baik. Misalnya, investasi di sektor energi terbarukan, transportasi ramah lingkungan, atau pertanian organik. Dalam dunia industri baik swasta maupun pemerintah tidak banyak juga perusahaan perusahaan yang seolah olah sudah mengikuti kebijakan Green finance namun tetap memberikan dampak yang buruk / pencemaran bagi lingkungan. Atas dasar tersebut perlu adanya sebuah analisa terhadap penerepan Green Finance pada sebuah instansi industri.

### 2.2 Landasan Teori Analisa Green Finance

1. Peraturan Otoritas Jasa Keuangan  (OJK) No. 51/POJK.03/2017 tentang Penerapan Prinsip-Prinsip Sustainable Finance bagi Lembaga Jasa Keuangan: Peraturan ini  di keluarkan oleh OJK untuk mendorong lembaga jasa keuangan, termasuk bank, untuk mengintegrasikan prinsip-prinsip keuangan berkelanjutan dalam kegiatan operasional dan bisnis mereka. 
2. Peraturan Pemerintah No. 47 Tahun 2017 tentang Penerapan Prinsip Ekonomi Hijau dalam Rencana Pembangunan Nasional: Peraturan ini mengatur strategi dan langkah-langkah untuk mendorong penerapan prinsip ekonomi hijau dalam pembangunan nasional, termasuk dalam hal pembiayaan proyek-proyek yang ramah lingkungan.

## 3. 📊 Metodologi

### 3.1 Metode Analisis

Penelitian ini menggunakan pendekatan kuantitatif berbasis data tabel untuk mengevaluasi kelayakan dan dampak proyek-proyek energi hijau melalui kerangka kerja Green Finance. Terdapat lima sumber data yang dianalisis: data finansial, data lingkungan, data sosial, data ekonomi, dan data geospasial.

Tahapan Penelitian:
**1. Pengumpulan Data**
  Lima dataset dikompilasi, masing-masing mewakili dimensi / gambaran Green Finance:

- Financial Dataset
- Environmental Dataset
- Social Dataset
- Economic Dataset
- Geospatial Dataset

**2.Pra-Pemrosesan Data**

- Mengimpor data dari file .xlsx
- Menggabungkan data untuk menganalis dari beberbagai sumber dan menjadikan nya menjadi 1 data.
- Pembersihan data: menangani nilai hilang, duplikat, dan format tidak konsisten
- Normalisasi dan transformasi kolom jika diperlukan

### 3.2 Implementasi 

Proyek ini dibangun menggunakan bahasa Python 3.12 dan dijalankan di lingkungan Jupyter Notebook dalam manajemen lingkungan Conda. Struktur direktori dan teknologi yang digunakan sebagai berikut:

### 3.3 📁 Struktur Proyek

- Python 3.12
- Conda (Environment Management)
- Jupyter Notebook
- Pandas, NumPy (manipulasi data)
- Matplotlib(visualisasi)
- OpenPyXL / xlrd (baca file Excel)

| Folder / File                  | Deskripsi                                                  |
|-------------------------------|-------------------------------------------------------------|
| `📁 notebooks/`                | Direktori untuk Jupyter Notebook                           |
| └── `analisis.ipynb`          | Notebook utama yang berisi proses eksplorasi dan analisis  |
| `📁 data/`                     | Folder berisi semua dataset proyek                         |
| ├── `financial_dataset.xlsx`  | Data investasi dan keuangan proyek                         |
| ├── `environmental_dataset.xlsx` | Data pengurangan emisi CO₂ dan aspek lingkungan        |
| ├── `social_dataset.xlsx`     | Data sosial seperti konflik dan status lahan               |
| ├── `economic_dataset.xlsx`   | Data dampak ekonomi proyek secara makro                    |
| └── `geospatial_dataset.csv`  | Data lokasi geografis dan efisiensi spasial proyek         |
| `README.md`                   | Dokumentasi utama proyek                                   |

Menetapkan library yang di perlukan untuk keseluruhan analisa 
```
# Import library yang diperlukan
import pandas as pd
import numpy as np
import matplotlib as plt
import openpyxl
```

Membaca data tabel Analisa kemudian pengolahan data untuk keseluruhan analisa  
```
# Ambil data excel sebagai berikut, misalnya :
env_df = pd.read_excel('D:/MATERI ETL/TUGAS GREEN FINANCE/Environmental_Dataset.xlsx')
fin_df = pd.read_excel('D:/MATERI ETL/TUGAS GREEN FINANCE/Financial_Dataset.xlsx')
soc_df = pd.read_excel('D:/MATERI ETL/TUGAS GREEN FINANCE/Social_Dataset.xlsx')
eco_df = pd.read_excel('D:/MATERI ETL/TUGAS GREEN FINANCE/Economic_Dataset.xlsx')
geo_df = pd.read_excel('D:/MATERI ETL/TUGAS GREEN FINANCE/Geospatial_Dataset.xlsx')
```

Menggabungkan data dari berbagai data yang berbeda untuk keseluruhan analisa 
```
# Setelah data terpanggil dengan env_df dan fin_df maka merge kedua file data tersebut sesuai kebutuhan, misal :
merged_df = pd.merge(env_df, fin_df, on='Project_ID', how='inner')
merged_df2 = pd.merge(eco_df, soc_df, on='Project_ID', how='inner')
```

### 4.1 Evaluasi Efisiensi Reduksi Emisi CO₂ pada Proyek PLTS

Analisis ini bertujuan untuk mengukur **efisiensi reduksi emisi karbon dioksida (CO₂)** terhadap biaya investasi pada proyek-proyek PLTS (Pembangkit Listrik Tenaga Surya). Efisiensi dihitung dengan rumus:

$$
\mathrm{Efisiensi}_{CO_2} = \frac{\mathrm{CO2\ Reduction\ (ton)}}{\mathrm{Investment\ Cost\ (Rp)}} = \frac{\mathrm{CO2\ Reduction}}{\mathrm{InvestmentCost} \times 1{,}000{,}000}
$$

Keterangan :
- **CO₂ Reduction** = total emisi CO₂ yang berhasil dikurangi (dalam ton)
- **Investment Cost** = jumlah biaya investasi proyek (dalam miliar rupiah)
