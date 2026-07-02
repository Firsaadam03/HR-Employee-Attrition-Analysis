# HR Employee Attrition Analysis

Analisis eksploratif dan visualisasi data terhadap dataset **IBM HR Employee Attrition**, dengan fokus pada identifikasi pola dan faktor pendorong resign karyawan menggunakan pendekatan *data storytelling*.

> Notebook ini merupakan bagian dari program **Job Connector Data Science & Machine Learning** (Purwadhika) — modul *Data Visualization*.

---

## Ringkasan

Dataset berisi **1.470 data karyawan IBM** dengan overall attrition rate **16.1%**. Analisis mengungkap profil karyawan berisiko resign yang konsisten di berbagai sudut pandang:

> **Muda (< 35 tahun) + bergaji rendah (< USD 3.500) + masa kerja singkat (< 3 tahun) + rutin lembur**

Kelompok paling kritis: **Sales Representative** (attrition 39.8%), **Laboratory Technician** (23.9%), dan karyawan **OverTime** (30.5%).

---

## Struktur Notebook

| Bagian | Deskripsi |
|---|---|
| **A. Import Libraries & Load Data** | Setup environment (pandas, numpy, matplotlib, seaborn) dan load dataset |
| **B. Data Cleaning** | Drop kolom konstan, konversi tipe data, label encoding untuk kolom ordinal (satisfaction & education) |
| **C. Latihan Visualisasi** | 15 visualisasi berjenjang (🟢 Starter → 🔵 Petunjuk Kolom → 🟣 Mandiri → 🔴 Advanced), masing-masing dengan insight terstruktur (Observasi & Interpretasi) |
| **D. Ringkasan Temuan & Rekomendasi** | Executive summary dan 3 rekomendasi prioritas berbasis data |

### Visualisasi yang Dibahas

1. Distribusi usia karyawan (Histogram)
2. Gaji karyawan lembur vs tidak lembur (Boxplot)
3. Tren rata-rata gaji berdasarkan lama bekerja (Line Chart)
4. Hubungan usia dan gaji bulanan (Scatter Plot)
5. Jumlah karyawan per department (Bar Chart)
6. Proporsi tingkat pendidikan (Pie Chart)
7. Distribusi gaji: resign vs tidak (Histogram)
8. Work-life balance per department (Boxplot)
9. Attrition rate per job role (Horizontal Bar Chart)
10. Pola satisfaction score per department (Heatmap)
11. Komposisi overtime per department (Stacked Bar Chart)
12. Jarak rumah dan kecenderungan resign (Bar Chart)
13. Distribusi gaji & lama bekerja: resign vs tidak (Histogram + Boxplot)
14. Marital status dan attrition rate per job role (Stacked Bar + Bar Chart)
15. Faktor satisfaction: resign vs tidak (Heatmap + Bar Chart)

---

## Temuan Utama

- **Usia**: Karyawan resign memiliki median usia 33.6 tahun, 4 tahun lebih muda dari yang bertahan (37.6 tahun).
- **Gaji**: Median gaji karyawan resign (USD 3.202) 38.5% lebih rendah dibanding yang bertahan (USD 5.204).
- **Overtime**: Karyawan lembur memiliki attrition rate 30.5%, hampir 3× lipat dibanding yang tidak lembur (10.4%).
- **Job Role**: Sales Representative adalah posisi paling berisiko (attrition 39.8%), 2.5× di atas rata-rata keseluruhan.
- **Masa kerja**: Karyawan dengan masa kerja < 2 tahun memiliki attrition rate 29.8%, hampir 2× lipat karyawan dengan masa kerja > 5 tahun.
- **Jarak rumah**: Attrition meningkat seiring jarak tempat tinggal — dari 14.0% (dekat) menjadi 22.1% (jauh).
- **Status pernikahan**: Karyawan *Single* memiliki attrition rate 25.5%, 2× lipat karyawan *Married* (12.5%).
- **Satisfaction**: JobSatisfaction dan EnvironmentSatisfaction adalah pembeda terbesar antara karyawan resign vs bertahan.

## Rekomendasi Prioritas

| Prioritas | Intervensi | Target | Timeline |
|---|---|---|---|
| 🔴 #1 | Audit & koreksi gaji karyawan < USD 3.000 dengan masa kerja < 2 tahun | Turunkan attrition entry-level dari ~30% ke ≤ 18% | 3 bulan |
| 🟠 #2 | Redesign insentif Sales Representative + overtime cap company-wide | Turunkan attrition Sales Rep dari 39.8% ke ≤ 25% | 6 bulan |
| 🟡 #3 | Program "First 3 Years Retention" (milestone bonus + guaranteed salary review) | Turunkan attrition 0–2 tahun masa kerja dari 29.8% ke ≤ 18% | 12 bulan |

---

## Dataset

- **Nama**: IBM HR Employee Attrition
- **Jumlah data**: 1.470 baris, tanpa missing value
- **File**: `HR-Employee-Attrition.csv` 

## Tools & Libraries

- Python 3
- pandas, numpy
- matplotlib, seaborn

## Cara Menjalankan

```bash
git clone <repo-url>
cd <repo-folder>
pip install pandas numpy matplotlib seaborn
jupyter notebook HR-Employee_Attritio_Analysis.ipynb
```

Pastikan file `HR-Employee-Attrition.csv` sudah berada di direktori yang sama dengan notebook.

---

*Catatan: Seluruh angka dalam insight berdasarkan data aktual dari dataset IBM HR Employee Attrition (n=1.470). Notebook ini adalah referensi jawaban — bukan satu-satunya pendekatan yang benar; grafik dapat bervariasi selama prinsip data storytelling terpenuhi.*
