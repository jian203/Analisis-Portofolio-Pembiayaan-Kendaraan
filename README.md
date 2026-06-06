# Analisis-Portofolio-Pembiayaan-Kendaraan
Analisis tren kredit kendaraan, performa cabang, segmentasi nasabah, dan forecast pembayaran 

## 📌 Latar Belakang
Proyek ini mensimulasikan peran seorang Data Analyst di perusahaan multifinance (pembiayaan kendaraan).
Menggunakan dataset L&T Financial Services dengan 233.154 transaksi pembiayaan kendaraan,
proyek ini bertujuan mengidentifikasi tren, pola risiko, dan memberikan rekomendasi bisnis
yang dapat ditindaklanjuti oleh manajemen.

---

## 🎯 Pertanyaan Bisnis
1. Berapa tingkat gagal bayar keseluruhan portofolio?
2. Apakah jenis pekerjaan mempengaruhi risiko gagal bayar?
3. Apakah LTV (Loan to Value) berkorelasi dengan risiko gagal bayar?
4. Kelompok usia berapa yang paling berisiko gagal bayar?
5. Seberapa efektif skor kredit dalam memprediksi gagal bayar?

---

## 📊 Temuan Utama & Insight Bisnis

### 1. Tingkat Gagal Bayar Keseluruhan
- **21.7%** nasabah gagal bayar cicilan pertama (50.611 dari 233.154 nasabah)
- Angka ini jauh di atas standar industri multifinance yang sehat (<5% NPL)
- **Rekomendasi:** Perlu evaluasi menyeluruh terhadap proses credit scoring dan persetujuan kredit

### 2. Jenis Pekerjaan vs Gagal Bayar
- Wiraswasta (Self Employed): **22.69%** gagal bayar
- Karyawan Tetap (Salaried): **20.35%** gagal bayar
- Selisih hanya 2.3% — jenis pekerjaan bukan faktor penentu utama
- **Rekomendasi:** Tidak perlu diskriminasi berlebihan berdasarkan jenis pekerjaan, fokus ke faktor lain

### 3. LTV (Loan to Value) vs Gagal Bayar
- LTV < 60%: **13.9%** gagal bayar (risiko terendah)
- LTV 60–75%: **19.6%** gagal bayar
- LTV 75–90%: **24.6%** gagal bayar ← segmen terbesar (126.463 nasabah!)
- LTV > 90%: **22.6%** gagal bayar
- **Rekomendasi:** Perketat syarat uang muka minimum untuk nasabah LTV > 75%

### 4. Usia Nasabah vs Gagal Bayar
- Usia < 25 tahun: **24.1%** gagal bayar (tertinggi)
- Usia 25–34 tahun: **22.2%** gagal bayar
- Usia 35–44 tahun: **20.4%** gagal bayar
- Usia 45+ tahun: **19.8%** gagal bayar (terendah)
- **Rekomendasi:** Nasabah di bawah 25 tahun perlu persyaratan tambahan (guarantor/co-borrower)

### 5. Skor Kredit vs Gagal Bayar
- B — Very Low Risk: **13.1%** gagal bayar (terendah)
- M — Very High Risk: **30.5%** gagal bayar (tertinggi — 2.3x lebih berisiko!)
- **116.950 nasabah (50.1%)** tidak memiliki riwayat kredit → gagal bayar 23.1%
- **Rekomendasi:** Nasabah tanpa riwayat kredit diperlakukan setara medium-high risk

---

## 🛠️ Tools & Teknologi
- **Python** (Google Colab)
- **Pandas** — data cleaning & manipulasi
- **Matplotlib & Seaborn** — visualisasi data
- **Dataset:** L&T Vehicle Loan Default Prediction (Kaggle)

---

## 📁 Struktur File

```text
├── notebook_analisis.ipynb       # Notebook utama (cleaning + EDA + insight)
├── dashboard_final.png           # Dashboard ringkasan 4 chart
├── chart1_distribusi.png         # Chart distribusi gagal bayar
├── chart2_employment.png         # Chart jenis pekerjaan
├── chart3_ltv.png                # Chart LTV vs gagal bayar
├── chart4_usia.png               # Chart usia vs gagal bayar
├── chart5_skorkreditdefault.png  # Chart skor kredit
├── LICENSE
└── README.md
```
