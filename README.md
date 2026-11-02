# Dataset Putusan Narkotika - [NAMA PN] ([TAHUN])

Dataset 50 dokumen putusan pengadilan perkara **Narkotika dan Psikotropika** (Pidana Khusus) dari **[NAMA PENGADILAN NEGERI]**, dikumpulkan sebagai bahan penelitian dan praktikum **Temu Kembali Informasi (Information Retrieval)**.

> Tugas UTS Temu Kembali Informasi, Semester Ganjil 2026/2027, Fakultas Teknik, Universitas Muhammadiyah Malang.

---

## Daftar Isi
1. [Tentang Dataset](#tentang-dataset)
2. [Sumber Data](#sumber-data)
3. [Struktur Repository](#struktur-repository)
4. [Struktur Overview.xlsx](#struktur-overviewxlsx)
5. [Statistik Dataset](#statistik-dataset)
6. [Cara Menggunakan](#cara-menggunakan)
7. [Kriteria Pemilihan Data](#kriteria-pemilihan-data)
8. [Catatan Etika dan Lisensi](#catatan-etika-dan-lisensi)
9. [Tim Penyusun](#tim-penyusun)

## Tentang Dataset
Putusan pengadilan adalah dokumen terbuka yang kaya informasi: identitas terdakwa, dakwaan, tuntutan, barang bukti, pertimbangan hakim, dan amar putusan. Dataset ini mengumpulkan **50 putusan** perkara narkotika agar dapat dipakai untuk:
- ekstraksi informasi (barang bukti, amar putusan, pasal yang didakwakan),
- preprocessing dan pengindeksan teks hukum berbahasa Indonesia,
- eksperimen pencarian (TF-IDF, BM25, dan model lain).

## Sumber Data
- Situs: [Direktori Putusan Mahkamah Agung RI](https://putusan3.mahkamahagung.go.id/direktori.html)
- Direktori: **Pidana Khusus**, klasifikasi **Narkotika dan Psikotropika**
- Pengadilan: **[NAMA PN]**
- Tahun putusan: **[TAHUN]**
- Tanggal pengambilan data: **[TANGGAL]**
- Seluruh putusan berstatus **bukan berkekuatan hukum tetap**.

## Struktur Repository
```
Dataset-Narkotika_329_317/
├── README.md
├── Dataset/
│   └── Narkotika.zip        # 50 putusan (*.pdf)
└── Overview/
    └── Overview.xlsx        # ringkasan 50 putusan
```

## Struktur Overview.xlsx
| Kolom | Isi |
|---|---|
| No | Nomor urut (1-50) |
| No Putusan | Nomor perkara, contoh: `408/Pid.Sus/2021/PN Gpr` |
| Lembaga Peradilan | Nama pengadilan, contoh: `PN Kab Kediri` |
| Barang Bukti | Barang bukti yang ditetapkan dalam putusan |
| Amar Putusan | Isi amar putusan (pidana penjara, denda, penetapan barang bukti, biaya perkara) |

## Statistik Dataset
| Item | Nilai |
|---|---|
| Jumlah putusan | 50 |
| Pengadilan | [NAMA PN] |
| Rentang tahun | [TAHUN] |
| Jenis narkotika dominan | [mis. sabu-sabu] |
| Rentang pidana penjara | [min] - [maks] |

## Cara Menggunakan
```bash
git clone https://github.com/Alfian79/Dataset-Narkotika_329_317.git
cd Dataset-Narkotika_329_317
unzip Dataset/Narkotika.zip -d Dataset/Narkotika
```
Membaca Overview dengan Python:
```python
import pandas as pd
df = pd.read_excel("Overview/Overview.xlsx")
print(df.head())
```

## Kriteria Pemilihan Data
1. Direktori Pidana Khusus, klasifikasi Narkotika dan Psikotropika.
2. Satu Pengadilan Negeri, tidak sama dengan kelompok lain.
3. Tahun putusan 2023-2025.
4. Bukan putusan berkekuatan hukum tetap.
5. Format dokumen PDF, 50 berkas.

## Catatan Etika dan Lisensi
Dokumen bersumber dari publikasi resmi Mahkamah Agung RI yang bersifat terbuka. Dataset hanya untuk keperluan akademik. Nama dan data pribadi dalam putusan tidak boleh disalahgunakan.

## Tim Penyusun
| Nama | NIM |
|---|---|
| Dino Alfian Zamri | 202310370311329 |
| [NAMA ANGGOTA 2] | [NIM ANGGOTA 2 (berakhiran 317)] |

Dosen pengampu: Galih W. W
