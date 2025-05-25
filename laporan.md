#Laporan Proyek Machine Learning

# Judul Proyek

Sistem Rekomendasi Artikel Menggunakan Content-Based Filtering

Disusun oleh:

Nama: Benny Alaster

Tanggal: 25 Mei 2025

# Daftar Isi

Project Overview

Business Understanding

Data Understanding

Data Preparation

Modeling

Evaluation

Kesimpulan

# 1. Project Overview

Proyek ini bertujuan membangun sistem rekomendasi artikel berbasis konten (content-based filtering) yang dapat memberikan saran artikel lain yang mirip berdasarkan isi artikel yang sedang dibaca. Sistem ini dibangun menggunakan Python dan berbagai pustaka machine learning dan NLP seperti scikit-learn dan NLTK.

Dataset yang digunakan berasal dari Kaggle - Article Recommendation System, yang terdiri dari judul dan isi artikel.

# 2. Business Understanding

Dalam dunia digital, banyak platform artikel menghadapi masalah dalam menjaga keterlibatan pengguna. Rekomendasi artikel yang relevan dapat meningkatkan waktu kunjungan dan pengalaman pengguna.

Rumusan Masalah:

Bagaimana membangun sistem yang dapat merekomendasikan artikel lain berdasarkan konten artikel yang sedang dibaca?

Tujuan:

Membangun sistem rekomendasi berbasis content-based filtering yang menyarankan artikel relevan.

# 3. Data Understanding

Dataset terdiri dari dua kolom utama:

Titles: Judul artikel

Article: Isi artikel

Contoh:

Title: "Best Books to Learn Computer Vision"

Article: Teks artikel lengkap

Jumlah data: 32 artikel

Tidak ditemukan data kosong atau duplikat. Semua artikel ditulis dalam bahasa Inggris.

# 4. Data Preparation

Tahapan preprocessing yang dilakukan:

Menggabungkan kolom Titles dan Article

Konversi ke huruf kecil

Menghapus angka dan tanda baca

Tokenisasi

Stopwords removal (menghapus kata-kata umum)

Stemming menggunakan PorterStemmer

Setelah preprocessing, dilakukan vektorisasi menggunakan TF-IDF untuk menghasilkan representasi numerik dari teks artikel.

# 5. Modeling

Metode yang digunakan:

Content-Based Filtering: Menggunakan cosine similarity antara vektor TF-IDF untuk mencari artikel yang paling mirip.

Fungsi get_recommendations dikembangkan untuk menerima input indeks artikel dan mengembalikan top-N rekomendasi artikel mirip.

# 6. Evaluation

Evaluasi dilakukan secara kualitatif (manual) karena dataset tidak menyediakan label relevansi atau interaksi pengguna.

Contoh:

Artikel utama: "Multiclass Classification Algorithms in Machine Learning"

1. Clustering Algorithms in Machine Learning

2. Use Cases of Different Machine Learning Algorithms

3. News Classification with Machine Learning

4. Best Books to Learn Deep Learning

5. Assumptions of Machine Learning Algorithms

Rekomendasi tersebut relevan secara tematik, menunjukkan bahwa sistem bekerja dengan baik dalam mengenali kesamaan topik.

# 7. Kesimpulan

Sistem rekomendasi artikel berbasis content-based filtering berhasil dibangun dan diuji dengan dataset artikel publik. Sistem dapat memberikan rekomendasi artikel relevan berdasarkan kemiripan konten.

Kelebihan:

Tidak membutuhkan data pengguna

Efektif jika deskripsi artikel kaya informasi

Keterbatasan:

Tidak mempertimbangkan preferensi pengguna

Tidak ada metrik kuantitatif tanpa label relevansi

Pengembangan ke depan:

Menggabungkan dengan collaborative filtering jika tersedia data interaksi pengguna

Membuat UI yang memungkinkan pengguna memilih artikel berdasarkan judul

