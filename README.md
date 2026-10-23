
# Analisis Data Supermarket dengan Algoritma Apriori

## Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis data pembelian barang supermarket menggunakan teknik data mining. Analisis dilakukan untuk mengetahui barang yang paling sering dibeli, pola pembelian pelanggan, serta hubungan antarbarang menggunakan algoritma Apriori.

## Tujuan

- Mengetahui karakteristik dan kualitas dataset.
- Melakukan pembersihan dan transformasi data.
- Mengidentifikasi barang yang paling sering muncul.
- Menganalisis tren pembelian berdasarkan waktu.
- Menemukan pola hubungan antarbarang menggunakan algoritma Apriori.
- Mengevaluasi aturan asosiasi menggunakan support, confidence, dan lift.

## Dataset

Nama dataset: Groceries Dataset

File dataset: `data/raw/Groceries_dataset.csv`

Kolom utama:
- `Member_number`: identitas member.
- `Date`: tanggal pembelian.
- `itemDescription`: nama barang yang dibeli.

Dataset berisi catatan barang yang dibeli oleh member pada tanggal tertentu. Karena tidak tersedia ID transaksi khusus, keranjang transaksi dibentuk berdasarkan kombinasi member dan tanggal. Pengelompokan tersebut merupakan asumsi analisis.

## Metode Analisis

### 1. Data Understanding
Memeriksa struktur dataset, jumlah baris dan kolom, tipe data, nilai kosong, data duplikat, serta jumlah kategori unik.

### 2. Data Cleaning
Membersihkan spasi pada nama barang, mengonversi format tanggal, dan memeriksa kualitas data. Data duplikat dievaluasi tanpa langsung menghapusnya secara sembarangan.

### 3. Exploratory Data Analysis
Melakukan analisis statistik dan visualisasi untuk melihat frekuensi barang, tren pembelian bulanan, distribusi keranjang, dan perilaku member.

### 4. Association Rule Mining
Menggunakan algoritma Apriori untuk menemukan kombinasi barang yang sering muncul bersama.

Parameter awal:
- Minimum support: 0.005
- Minimum confidence: 0.1

### 5. Evaluasi Aturan Asosiasi

- Support: proporsi keranjang yang mengandung kombinasi barang.
- Confidence: tingkat kemunculan barang akibat ketika barang sebab muncul.
- Lift: ukuran kekuatan hubungan dibandingkan dengan kemunculan independen.

Interpretasi lift:
- Lift > 1: asosiasi positif.
- Lift = 1: tidak menunjukkan asosiasi.
- Lift < 1: asosiasi negatif.

## Struktur Proyek

```text
analisis-data-supermarket/
├── data/
│   └── raw/
│       └── Groceries_dataset.csv
├── output/
│   ├── grafik_cleaning_transformasi.png
│   ├── grafik_barang_terpopuler.png
│   ├── grafik_aturan_asosiasi.png
│   ├── grafik_tren_pembelian_bulanan.png
│   ├── grafik_distribusi_keranjang.png
│   ├── grafik_ringkasan_statistik.png
│   ├── grafik_distribusi_member.png
│   ├── grafik_tren_10_barang.png
│   ├── grafik_korelasi_barang.png
│   ├── grafik_evaluasi_apriori.png
│   └── laporan_ringkasan_dataset.csv
├── analisis_data.ipynb
├── README.md
└── requirements.txt
```

Nama file pada struktur di atas merupakan daftar hasil yang direncanakan. File yang belum berhasil dibuat atau belum diunggah perlu disesuaikan dengan isi repositori sebenarnya.

## Teknologi yang Digunakan

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Mlxtend
- Jupyter Notebook
- Visual Studio Code
- Git dan GitHub

## Cara Menjalankan Proyek

1. Unduh atau clone repositori ini.
2. Buka folder proyek di Visual Studio Code.
3. Instal pustaka yang diperlukan.
4. Buka `analisis_data.ipynb`.
5. Jalankan cell secara berurutan dari atas ke bawah.
6. Periksa tabel statistik, grafik, dan file CSV yang dihasilkan pada folder `output`.

Instalasi pustaka:

```bash
pip install pandas numpy matplotlib seaborn mlxtend jupyter
```

## Hasil yang Diharapkan

Proyek ini menghasilkan informasi mengenai karakteristik dataset, barang yang sering dibeli, tren pembelian, distribusi keranjang, dan aturan asosiasi antarbarang.

Hasil aturan asosiasi dapat digunakan sebagai informasi pendukung untuk memahami pola pembelian pelanggan. Temuan tersebut bersifat eksploratif dan tidak secara langsung membuktikan hubungan sebab-akibat.

## Kesimpulan

Analisis data supermarket dengan algoritma Apriori dapat membantu mengidentifikasi pola kemunculan barang secara bersamaan. Penggunaan statistik deskriptif, visualisasi, dan evaluasi aturan asosiasi memberikan gambaran yang lebih terstruktur mengenai karakteristik dataset dan pola pembelian pelanggan.
