# Optimasi Strategi Pemasaran (Data Analysis Project)

## Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis data penjualan e-commerce guna memahami pola penjualan, perilaku pelanggan, serta efektivitas strategi pemasaran. Analisis dilakukan menggunakan Python dengan pendekatan data cleaning, visualisasi, dan analisis bisnis seperti RFM.

---

## Business Question

Analisis ini dilakukan untuk menjawab beberapa pertanyaan berikut:

* Produk apa yang memiliki harga tinggi tetapi penjualannya rendah (underperformer)?
* Siapa pelanggan terbaik berdasarkan perilaku transaksi?
* Kategori produk mana yang paling efisien dalam penggunaan anggaran iklan?
* Apakah peningkatan anggaran iklan berpengaruh terhadap peningkatan penjualan?

---

## Data Wrangling

Sebelum melakukan analisis, dilakukan proses pembersihan data sebagai berikut:

* Mengubah tipe data `Order_Date` menjadi format datetime
* Mengisi nilai kosong pada kolom `Total_Sales` dengan perhitungan:
  Total_Sales = Quantity × Price_Per_Unit
* Menghapus data yang tidak valid seperti:

  * Quantity ≤ 0
  * Price_Per_Unit ≤ 0
  * Ad_Budget ≤ 0
* Menambahkan kolom `Month` untuk analisis tren penjualan bulanan

Setelah proses ini, data menjadi bersih dan siap digunakan.

---

## Insights

### Tren Penjualan Bulanan

Penjualan menunjukkan pola yang tidak stabil dari bulan ke bulan. Terdapat beberapa periode dengan peningkatan penjualan, yang kemungkinan dipengaruhi oleh faktor promosi atau waktu tertentu.

---

### Analisis Korelasi

Hasil analisis menunjukkan adanya hubungan positif antara `Ad_Budget` dan `Total_Sales`. Hal ini menunjukkan bahwa peningkatan anggaran iklan cenderung diikuti dengan peningkatan penjualan, meskipun pengaruhnya tidak terlalu kuat.

---

### Underperformer Product

Ditemukan bahwa produk dengan harga tinggi cenderung memiliki jumlah penjualan yang lebih rendah. Hal ini menunjukkan bahwa harga yang terlalu tinggi dapat menjadi salah satu faktor yang menghambat penjualan.

---

### RFM Analysis

Segmentasi pelanggan dilakukan berdasarkan:

* Recency (waktu sejak transaksi terakhir)
* Frequency (jumlah transaksi)
* Monetary (total pengeluaran)

Hasilnya menunjukkan bahwa:

* Pelanggan dengan nilai RFM tinggi merupakan pelanggan loyal
* Pelanggan dengan nilai rendah berpotensi tidak aktif atau berhenti bertransaksi

---

### Analisis Efisiensi Kategori

Hasil perbandingan antara `Total_Sales` dan `Ad_Budget` menunjukkan bahwa tidak semua kategori memiliki efisiensi yang sama. Beberapa kategori mampu menghasilkan penjualan tinggi dengan biaya iklan yang relatif kecil, sementara yang lain kurang efisien.

---

### Uji Hipotesis Iklan

Perbandingan antara kelompok dengan anggaran iklan tinggi dan rendah menunjukkan bahwa kelompok dengan anggaran lebih tinggi memiliki rata-rata penjualan yang lebih besar. Hal ini menunjukkan bahwa iklan memiliki pengaruh terhadap penjualan.

---

## Recommendation

Berdasarkan hasil analisis, beberapa rekomendasi yang dapat diberikan:

* Mengevaluasi harga produk yang tinggi tetapi memiliki penjualan rendah
* Memberikan perhatian lebih pada pelanggan loyal melalui program khusus
* Mengoptimalkan penggunaan anggaran iklan dengan fokus pada kategori yang lebih efektif
* Menggunakan data sebagai dasar dalam pengambilan keputusan pemasaran

---

## Kesimpulan

Dari hasil analisis yang dilakukan, dapat disimpulkan bahwa faktor harga, iklan, dan perilaku pelanggan memiliki pengaruh terhadap penjualan. Selain itu, penggunaan analisis data dapat membantu perusahaan dalam menentukan strategi pemasaran yang lebih efektif dan efisien.
