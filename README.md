# Analisis Data Supermarket

## Deskripsi
Proyek ini menganalisis data transaksi supermarket untuk mengetahui barang yang paling sering tercatat dan menemukan pola hubungan antarbarang.

## Dataset
- Sumber: [Groceries Dataset - Kaggle](https://www.kaggle.com/datasets/heeraldedhia/groceries-dataset)
- Jumlah data awal: 38.765 baris
- Jumlah variabel: 3
- Jumlah jenis barang: 167

## Metode
Analisis menggunakan tahapan CRISP-DM dan algoritma Apriori untuk menemukan aturan asosiasi antarbarang.

## Hasil Awal
- Barang yang paling sering tercatat: whole milk (2.502 kali).
- Kombinasi barang yang ditemukan: 126.
- Aturan asosiasi yang ditemukan: 19.
- Aturan dengan lift tertinggi: frankfurter → other vegetables, dengan lift 1,116.

## Tools
- Python
- Pandas
- Matplotlib
- Seaborn
- Mlxtend
- Visual Studio Code