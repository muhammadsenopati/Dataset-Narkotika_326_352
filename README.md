# Dataset-Narkotika_326_352

![Status](https://img.shields.io/badge/status-completed-success?style=for-the-badge)
![Domain](https://img.shields.io/badge/domain-dokumen%20hukum-blue?style=for-the-badge)
![Data](https://img.shields.io/badge/data-53%20putusan-orange?style=for-the-badge)
![Format](https://img.shields.io/badge/format-PDF%20%7C%20CSV%20%7C%20XLSX-purple?style=for-the-badge)

## Deskripsi

**Dataset-Narkotika_326_352** merupakan kumpulan data putusan perkara pidana narkotika dari Pengadilan Negeri Pekanbaru. Dataset ini disusun untuk mendukung penelitian dan pengembangan sistem pengolahan dokumen hukum, termasuk klasifikasi teks, pencarian putusan, ekstraksi informasi.

Dataset berisi **53 putusan unik** yang telah dikumpulkan, diperiksa, dan dirapikan dari dokumen PDF. Setiap putusan dirangkum ke dalam informasi penting berupa nomor putusan, lembaga peradilan, barang bukti, dan amar putusan.

## Identitas Proyek

| Keterangan | Informasi |
|---|---|
| Nama proyek | Dataset-Narkotika_326_352 |
| Kelas | Temu Kembali Informasi A |
| Sumber dokumen | Direktori Putusan Mahkamah Agung Republik Indonesia |
| Jenis perkara | Pidana narkotika dan perkara terkait |
| Lembaga peradilan | Pengadilan Negeri Pekanbaru |
| Jumlah putusan | 53 putusan unik |
| Periode putusan | 2024–2026 |
| Format sumber | PDF |
| Format data terstruktur | CSV dan XLSX |

## Struktur Folder

```text
Dataset-Narkotika_326_352/
├── Dataset 326-352/
│   ├── Narkotika_*.zip
├── Overview 326-352/
│   ├── Overview.xlsx
└── README.md
```

## Isi Dataset Terstruktur

File CSV dan XLSX memiliki lima atribut utama:

| Atribut | Deskripsi |
|---|---|
| `No` | Nomor urut data |
| `No Putusan` | Nomor resmi putusan pengadilan |
| `Lembaga Peradilan` | Pengadilan yang menerbitkan putusan |
| `Barang Bukti` | Ringkasan barang bukti dalam perkara |
| `Amar Putusan` | Ringkasan keputusan atau hukuman pengadilan |

## Contoh Data

```text
No Putusan: 718/Pid.Sus/2024/PN Pbr
Lembaga: PN Pekanbaru
Barang bukti: pipa kaca, alat hisap, dan telepon seluler
Amar putusan: terdakwa dinyatakan terbukti bersalah dan dijatuhi pidana sesuai amar putusan
```

## Proses Pengolahan Data

1. Mengumpulkan dokumen putusan dalam format PDF.
2. Memeriksa nomor dan identitas setiap putusan.
3. Menghapus salinan dokumen yang sama agar tidak terjadi duplikasi.
4. Mengekstrak informasi barang bukti dan amar putusan.
5. Menyusun ringkasan ke dalam format CSV.
6. Mengonversi data terstruktur ke format XLSX.
7. Menyusun overview untuk membantu pemeriksaan dan pemahaman dataset.

## Kegunaan Dataset

Dataset ini dapat digunakan untuk:

- klasifikasi dokumen putusan;
- pencarian putusan berdasarkan kata kunci;
- ekstraksi entitas hukum;
- analisis kemiripan perkara;
- pengembangan sistem Case-Based Reasoning;
- pembuatan ringkasan dokumen hukum;
- eksperimen Natural Language Processing (NLP) berbahasa Indonesia.

## Catatan Validasi

- Setiap nomor putusan dihitung satu kali meskipun terdapat file salinan dengan nama `(1)`, `(2)`, atau format ZIP.
- Dokumen yang tersedia merupakan putusan tingkat pertama Pengadilan Negeri Pekanbaru.
- Status **berkekuatan hukum tetap (inkracht)** tidak digunakan sebagai label karena sebagian PDF tidak mencantumkan keterangan eksplisit mengenai status tersebut.
- Ringkasan barang bukti dan amar putusan dibuat berdasarkan isi dokumen PDF. Untuk kebutuhan hukum formal, dokumen putusan asli tetap menjadi rujukan utama.

## Format Penggunaan

### Membaca CSV dengan Python

```python
import pandas as pd

df = pd.read_csv("Dataset 326-352/dataset_putusan_pn_pbr.csv")
print(df.head())
print(df.shape)
```

### Membaca XLSX dengan Python

```python
import pandas as pd

df = pd.read_excel("Dataset 326-352/dataset_putusan_pn_pbr.xlsx")
print(df.head())
```

## Kontributor

| Nama | NIM |
|---|---|
| Muhammad Senopati Panotogomo | 202310370311326 |
| Ken Irgi Putra Rudiansyah | 202310370311352 |

## Lisensi dan Etika Penggunaan

Dataset ini digunakan untuk kepentingan akademik dan penelitian. Data tidak boleh digunakan untuk menggantikan nasihat hukum, mengambil keputusan hukum otomatis, atau menyebarkan informasi pribadi di luar konteks penelitian.

Dokumen sumber tetap mengikuti ketentuan dan hak akses dari sumber resmi Direktori Putusan Mahkamah Agung Republik Indonesia.

---

**Dataset-Narkotika_326_352**  
Dokumentasi dataset putusan perkara narkotika untuk penelitian dokumen hukum berbasis data.
