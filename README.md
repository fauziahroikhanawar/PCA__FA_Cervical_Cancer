# Implementasi Principal Component Analysis (PCA) dan Factor Analysis (FA) pada Risiko Perilaku Kanker Serviks

## Deskripsi Proyek
Proyek ini menerapkan PCA dan Factor Analysis untuk mereduksi 19 variabel perilaku pada dataset Cervical Cancer Behavior Risk (UCI, 72 observasi). Uji asumsi Bartlett's Test dan KMO (0,73) menunjukkan data layak dianalisis. Eliminasi bertahap variabel dengan MSA rendah menghasilkan tiga komponen utama yang menjelaskan 73,4% total variansi, dengan rotasi Varimax mengelompokkan variabel menjadi faktor dukungan sosial, persepsi risiko, dan motivasi internal.

## Tujuan
- Menguji asumsi korelasi (Bartlett's Test) dan kelayakan sampel (KMO) pada variabel risiko perilaku kanker serviks.
- Melakukan eliminasi bertahap variabel dengan MSA rendah untuk meningkatkan validitas model.
- Membentuk faktor yang lebih ringkas untuk pemetaan profil risiko pasien secara efisien.

## Tools & Library
- R Programming, RStudio
- Package R: `psych`, `factoextra`, `ggplot2`, `dplyr`, `corrplot`
- RPubs (publikasi hasil)

## Tahapan Proyek
1. **Load Data** - Dataset Cervical Cancer Behavior Risk (72 observasi, 19 variabel perilaku)
2. **EDA** - Statistika deskriptif, boxplot, matriks korelasi
3. **Uji Asumsi** - Bartlett's Test (p-value < 0,05) & KMO (0,73)
4. **Eliminasi Bertahap** - Menghapus 5 variabel dengan MSA rendah (X1, X2, X5, X6, X7)
5. **PCA** - Ekstraksi 3 komponen utama dengan eigenvalue > 1
6. **Factor Analysis** - Rotasi Varimax untuk interpretasi faktor

## Hasil
| Tahap | Hasil |
|---|---|
| Dataset | 72 observasi, 19 variabel perilaku |
| Bartlett's Test | p-value = 6,85 × 10⁻⁸⁷ (signifikan) |
| KMO | 0,73 (layak, >0,5) |
| Variabel dieliminasi | 5 variabel (X1, X2, X5, X6, X7) |
| Jumlah komponen | 3 (eigenvalue > 1) |
| Total variansi | 73,4% (PC1: 38,5%, PC2: 24,5%, PC3: 10,4%) |

**Faktor hasil rotasi Varimax:**
1. **Faktor 1:** Dukungan sosial & pemberdayaan diri (X13-X19)
2. **Faktor 2:** Persepsi risiko & norma lingkungan (X8-X11)
3. **Faktor 3:** Motivasi internal & kebersihan diri (X3, X4, X12)

## File Terkait
- RPubs (Hasil Lengkap)<br>(https://rpubs.com/zhrraidaaa/Modul1PCA)
- Dataset: Cervical Cancer Behavior Risk (UCI)<br>(https://archive.ics.uci.edu/dataset/537/cervical+cancer+behavior+risk)

## Author
**Fauziah Roikhana Wardah** (dan tim)
- Program Studi S1 Sains Data, Universitas Negeri Surabaya
