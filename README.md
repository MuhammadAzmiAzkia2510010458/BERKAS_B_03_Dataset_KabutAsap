## Identitas Kelompok
- **Kelompok:** 3
- **Mata Kuliah:** Berkas Sistem
- **Program Studi:** Teknik Informatika
- **Universitas:** Universitas Islam Kalimantan Muhammad Arsyad Al Banjari

# Dataset Klasifikasi Ketebalan Kabut Asap

## 1. Deskripsi Dataset

Dataset ini merupakan kumpulan citra kabut asap di wilayah Indonesia pada tahun 2026 yang digunakan untuk keperluan pembelajaran dan pengembangan klasifikasi citra.

Dataset dikelompokkan menjadi tiga kategori berdasarkan tingkat ketebalan asap, yaitu:

- **Tipis:** Asap terlihat samar dan objek masih dapat terlihat dengan jelas.
- **Sedang:** Asap mulai menghalangi pandangan sehingga objek terlihat agak samar.
- **Tebal:** Asap terlihat pekat dan menghalangi pandangan sehingga objek sulit terlihat.

Setiap gambar dilengkapi metadata untuk mencatat informasi nama file, kategori asap, sumber gambar, URL sumber, fotografer, deskripsi, dan jarak pandang apabila tersedia.

## 2. Struktur Folder

```text
Dataset_KabutAsap/
├── README.md
├── metadata.csv
├── LICENSE
├── .gitignore
└── dataset/
    ├── tipis/
    ├── sedang/
    └── tebal/
```

## 3. Cara Mengunduh Dataset

Dataset dapat diunduh melalui beberapa cara berikut.

### A. Mengunduh melalui GitHub

1. Buka halaman repository GitHub.
2. Klik tombol **Code**.
3. Pilih **Download ZIP**.
4. Ekstrak file ZIP ke komputer.
5. Dataset siap digunakan.

### B. Mengunduh menggunakan Git

Jalankan perintah berikut pada terminal:

```bash
git clone https://github.com/MuhammadAzmiAzkia2510010458/BERKAS_B_03_Dataset_KabutAsap
```

## 4. Cara Menggunakan Dataset

1. Buka folder `Dataset_KabutAsap`.
2. Masuk ke folder `dataset`.
3. Pilih kategori gambar yang ingin digunakan:
   - `tipis`
   - `sedang`
   - `tebal`
4. Gunakan gambar sesuai kebutuhan pembelajaran atau pengujian klasifikasi citra.
5. Gunakan file `metadata.csv` untuk melihat informasi setiap gambar.

Contoh membaca dataset menggunakan Python:

```python
import os

folder_dataset = "dataset"

kategori = ["tipis", "sedang", "tebal"]

for kelas in kategori:
    folder = os.path.join(folder_dataset, kelas)

    jumlah = len([
        file for file in os.listdir(folder)
        if file.lower().endswith((".jpg", ".jpeg", ".png"))
    ])

    print(f"{kelas}: {jumlah} gambar")
```

## 5. Informasi Metadata

Informasi gambar disimpan dalam file `metadata.csv` dengan kolom berikut:

| Kolom | Keterangan |
|---|---|
| Nama File dan berada didalam folder | Lokasi file gambar dalam repository |
| Kondisi Asap | Kategori ketebalan asap |
| Sumber | Asal gambar atau dokumentasi |
| Sumber URL | Tautan halaman sumber gambar |
| Photographer | Nama fotografer atau pemilik dokumentasi |
| Deskripsi | Penjelasan singkat kondisi pada gambar |
| Jarak pandang | Informasi jarak pandang apabila tersedia |

## 6. Riwayat Commit Anggota Kelompok

https://github.com/MuhammadAzmiAzkia2510010458/BERKAS_B_03_Dataset_KabutAsap/commits/main/

| No. | Nama Anggota | NPM | Bukti Riwayat Commit Anggota |
|---|---|---|---|
| 1 | [Muhammad Azmi Azkia] | [2510010458] | [https://github.com/MuhammadAzmiAzkia2510010458/BERKAS_B_03_Dataset_KabutAsap/commits/main/?author=MuhammadAzmiAzkia2510010458] |
| 2 | [Nama Anggota 2] | [NPM] | [Link commit] |
| 3 | [Nama Anggota 3] | [NPM] | [Link commit] |
| 4 | [Nama Anggota 4] | [NPM] | [Link commit] |
| 5 | [Nama Anggota 5] | [NPM] | [Link commit] |

## 7. Sumber Dataset

Gambar dikumpulkan dari berbagai sumber dokumentasi mengenai kondisi kabut asap di Indonesia pada tahun 2026.

Informasi sumber gambar, fotografer, dan tautan sumber dicatat dalam file `metadata.csv` apabila tersedia.

## 8. Lisensi

Repository ini menggunakan lisensi
[Creative Commons Attribution 4.0 International (CC-BY-4.0)](https://creativecommons.org/licenses/by/4.0/).

Penggunaan kembali gambar tetap harus memperhatikan lisensi dan hak cipta
dari masing-masing pemilik gambar.

## 9. Catatan

Dataset dapat mengalami penambahan dan pembaruan selama proses pengumpulan data berlangsung.