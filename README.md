# TUGAS BESAR KOMPUTASI STATISTIKA - KELOMPOK 8 RB

## 📊 Prediksi Risiko Saham Perusahaan di Sumatera Bagian Selatan

[![Video Presentasi](https://img.shields.io/badge/Video-Presentasi-red?style=flat-square&logo=youtube)](https://drive.google.com/file/d/13MvYFG23kGek_6nTB22DKpP8W89pILSd/view?usp=sharing)

### 📝 Deskripsi Proyek

Proyek ini menganalisis dan memprediksi risiko portofolio saham dari tiga perusahaan besar di Sumatera Bagian Selatan menggunakan metode pembangkitan bilangan acak. Analisis dilakukan terhadap data historis 4 tahun terakhir untuk memproyeksikan risiko investasi dalam 30 hari ke depan.

**Perusahaan yang Dianalisis:**
- **PTBA (PT Bukit Asam Tbk)** - Perusahaan pertambangan batubara
- **SMBR (PT Semen Baturaja Tbk)** - Perusahaan semen
- **RMKE (PT Rukun Maju Bersama Elektrindo)** - Perusahaan distribusi listrik

### 🎯 Tujuan Penelitian

Mengukur risiko secara kuantitatif menggunakan metode pembangkitan bilangan acak untuk mensimulasikan return portofolio berbasis distribusi-t Student, dengan fokus pada:

1. **Estimasi Risiko**: Menghitung Value at Risk (VaR) portofolio dalam 30 hari ke depan
2. **Tingkat Kepercayaan**: Menentukan seberapa yakin terhadap prediksi risiko yang didapatkan
3. **Simulasi Monte Carlo**: Mensimulasikan berbagai skenario return portofolio

### 🔬 Metodologi

Proyek ini menggunakan dua metode utama dalam pembangkitan bilangan acak:

#### 1. **Inverse Transform Method**
- Digunakan untuk membangkitkan bilangan acak uniform U(0,1)
- Transformasi dari distribusi uniform ke distribusi target
- Memastikan bilangan acak yang dihasilkan mengikuti distribusi yang diinginkan

#### 2. **Acceptance-Rejection Method**
- Membangkitkan bilangan acak dari distribusi-t Student
- Menggunakan distribusi proposal Cauchy
- Cocok untuk distribusi yang kompleks seperti distribusi-t dengan degree of freedom tertentu

### 📂 Struktur Repository

```
TUGAS-BESAR-KOMSTAT-KELOMPOK_8-RB/
│
├── README.md                 # Dokumentasi proyek (file ini)
├── Dataset_8_RB.csv         # Data historis saham PTBA, SMBR, RMKE (4 tahun)
├── codeR_8_RB.ipynb         # Jupyter Notebook berisi analisis lengkap dalam R
├── Laporan_8_RB.pdf         # Laporan tertulis lengkap
├── PPT_8_RB.pptx            # Presentasi PowerPoint
└── Video_8_RB.mp4           # Video presentasi (link Google Drive)
```

### 📊 Dataset

**File**: `Dataset_8_RB.csv`

Dataset berisi data harga saham adjusted (disesuaikan) dari tiga perusahaan:
- **Periode**: November 2021 - November 2025 (4 tahun)
- **Kolom**:
  - `symbol`: Kode saham (PTBA.JK, SMBR.JK, RMKE.JK)
  - `date`: Tanggal transaksi
  - `adjusted`: Harga saham yang telah disesuaikan

### 💻 Cara Menggunakan

#### Prasyarat
Pastikan Anda telah menginstal:
- R (versi 4.0 atau lebih baru)
- Jupyter Notebook dengan kernel R
- Package R yang diperlukan:
  - `tidyquant` - Untuk mengunduh dan menganalisis data keuangan
  - `dplyr` - Untuk manipulasi data
  - `ggplot2` - Untuk visualisasi
  - `tidyr` - Untuk pembersihan data
  - `scales` - Untuk formatting

#### Instalasi Package

Buka R console atau Jupyter Notebook dan jalankan:

```r
install.packages("tidyquant")
install.packages("dplyr")
install.packages("ggplot2")
install.packages("tidyr")
install.packages("scales")
```

#### Menjalankan Analisis

1. **Clone Repository**
   ```bash
   git clone https://github.com/sains-data/TUGAS-BESAR-KOMSTAT-KELOMPOK_8-RB.git
   cd TUGAS-BESAR-KOMSTAT-KELOMPOK_8-RB
   ```

2. **Buka Jupyter Notebook**
   ```bash
   jupyter notebook codeR_8_RB.ipynb
   ```

3. **Jalankan Sel-sel Kode**
   - Jalankan sel instalasi package (hanya sekali)
   - Jalankan sel-sel berikutnya secara berurutan
   - Perhatikan output visualisasi dan hasil perhitungan

### 📈 Hasil Analisis

Notebook menghasilkan beberapa analisis penting:

1. **Distribusi Return Historis**: Visualisasi bentuk distribusi return harian portofolio
2. **Simulasi Acceptance-Rejection**: Demonstrasi visual metode AR untuk menghasilkan bilangan acak
3. **Simulasi Inverse Transform**: Demonstrasi visual metode IT untuk transformasi distribusi
4. **Value at Risk (VaR)**: Perhitungan risiko maksimum dengan tingkat kepercayaan tertentu
5. **Perbandingan Metode**: Evaluasi efisiensi kedua metode pembangkitan bilangan acak

### 🎓 Kontributor - Kelompok 8 RB

Tugas Besar Mata Kuliah Komputasi Statistika

### 📚 Referensi

1. Ross, S. M. (2013). *Simulation*. Academic Press.
2. Kroese, D. P., Taimre, T., & Botev, Z. I. (2011). *Handbook of Monte Carlo Methods*. John Wiley & Sons.
3. Jorion, P. (2007). *Value at Risk: The New Benchmark for Managing Financial Risk*. McGraw-Hill.

### 📄 Lisensi

Proyek ini dibuat untuk keperluan akademis dalam mata kuliah Komputasi Statistika.

### 📧 Kontak

Untuk pertanyaan atau diskusi lebih lanjut, silakan buka issue di repository ini.

---

**Catatan**: Hasil simulasi dan prediksi dalam proyek ini adalah untuk tujuan pembelajaran dan tidak boleh digunakan sebagai saran investasi.
