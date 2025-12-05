# Dataset Sentimen Kuliner – Lexicon Bahasa Indonesia & Banjar

Dataset ini merupakan kumpulan **kosakata sentimen (sentiment lexicon)** yang disusun untuk kebutuhan **analisis sentimen ulasan konsumen UMKM kuliner**. Dataset mencakup kata-kata dalam **Bahasa Indonesia** dan **Bahasa Banjar** yang ditemukan dalam komentar publik pada platform **Instagram** dan **TikTok**.

Dataset ini disusun melalui proses:
- kompilasi dari berbagai sumber teks,
- pembersihan dan normalisasi linguistik,
- penghapusan duplikasi,
- penyesuaian kata tidak baku,
- serta penentuan bobot sentimen berdasarkan konteks **kuliner**.

Dataset ini memperluas **InSet Lexicon**  
[InSet Lexicon – GitHub Repository](https://github.com/fajri91/InSet).
*Koto & Rahmaningtyas (2018)*  
melalui penambahan **kata baru** yang relevan dalam domain kuliner di Kalimantan Selatan.

---

## 📂 Isi Dataset

Dataset disimpan dalam dua file CSV:

1. **kata-sentimen-positif.csv**  
   Berisi daftar kosakata dengan nilai sentimen **positif**  
   *(jumlah data sesuai isi file)*

2. **kata-sentimen-negatif.csv**  
   Berisi daftar kosakata dengan nilai sentimen **negatif**  
   *(jumlah data sesuai isi file)*

Format kolom yang umum tersedia:
- `kata` — kosakata dalam Bahasa Indonesia atau Banjar  
- `nilai_sentimen` — bobot sentimen (mis. +1, +2, -1, -2)  
- `kategori` *(opsional)* — kategori konteks seperti rasa, layanan, kebersihan, dsb.

---

## Tujuan Penggunaan

Dataset ini dapat digunakan untuk:
- analisis sentimen berbasis lexicon,
- penelitian NLP sektor UMKM kuliner,
- pembentukan model hybrid (lexicon + machine learning),
- pembuatan alat monitoring opini publik,
- penguatan model klasifikasi sentimen Bahasa Indonesia dan Banjar.

---

## Cara Menggunakan (Python)

```python
import pandas as pd

positive = pd.read_csv("kata-sentimen-positif.csv")
negative = pd.read_csv("kata-sentimen-negatif.csv")

print(positive.head())
print(negative.head())
