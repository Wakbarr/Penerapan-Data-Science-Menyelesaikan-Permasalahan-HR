# Penyelesaian Tantangan Human Resources

## Pemahaman Bisnis

Jaya Jaya Maju adalah perusahaan multinasional yang berdiri sejak tahun 2000 dan memiliki lebih dari 1.000 karyawan di berbagai wilayah. Meskipun telah berkembang pesat, perusahaan ini menghadapi masalah tingginya tingkat attrition (pergantian karyawan) yang melebihi 10%. Kondisi ini berisiko meningkatkan biaya rekrutmen, menurunkan produktivitas, dan mengganggu stabilitas organisasi.

### Permasalahan Utama

1. **Faktor Penyebab Attrition Tinggi**
   Menentukan variabel apa saja yang paling berpengaruh terhadap keputusan karyawan untuk keluar dari perusahaan.

2. **Desain Visualisasi Data yang Efektif**
   Membuat grafik dan laporan yang mudah dipahami agar tim HR dapat memantau metrik utama secara real-time.

3. **Proyeksi Risiko Keluar Karyawan**
   Membangun model prediktif untuk mengidentifikasi karyawan dengan kemungkinan tinggi meninggalkan perusahaan sehingga dapat diintervensi lebih awal.

### Ruang Lingkup Proyek

1. **Analisis Data Karyawan**

   * Melakukan eksplorasi data untuk menemukan pola dan insight terkait attrition.
   * Mengidentifikasi fitur paling krusial yang berkaitan dengan keputusan karyawan untuk resign.

2. **Pembuatan Dashboard Bisnis**

   * Menyajikan tampilan interaktif untuk memonitor faktor-faktor kunci attrition.
   * Menyediakan panel kontrol bagi manajer HR untuk mengambil keputusan berbasis data.

3. **Pengembangan Model Prediksi**

   * Melatih model machine learning untuk memperkirakan potensi attrition tiap individual.
   * Memprioritaskan tindakan pencegahan bagi karyawan berisiko.

4. **Rekomendasi dan Tindak Lanjut**

   * Memberikan saran strategi HR berdasarkan hasil analisis dan prediksi.

## Data dan Persiapan Lingkungan

* **Sumber Data:** Dataset karyawan lengkap dengan informasi demografis, pengalaman, kompensasi, dan departemen, tersedia di: [https://github.com/dicodingacademy/dicoding\_dataset/blob/main/employee/employee\_data.csv](https://github.com/dicodingacademy/dicoding_dataset/blob/main/employee/employee_data.csv)
* **Lingkungan Kerja:**

  * Python 3.9 dengan library seperti Pandas, Scikit-learn, SQLAlchemy.
  * Metabase dijalankan via Docker pada port `3000`.
* **Langkah Awal:**

  1. Clone repo projek.
  2. Buat environment Conda `hr_project`.
  3. Install requirement.
  4. Jalankan Metabase dan sambungkan database Supabase.

## Komponen Dashboard

1. **Tinjauan Umum**

   * **Total Karyawan:** 1.058 orang.
   * **Jumlah Attrition:** 179 orang.
   * **Persentase:** 16,92% dari total karyawan.

2. **Faktor-Faktor Kunci**

   * **Overtime:** 54,7% karyawan lembur resign.
   * **Status Pernikahan:** Single (94 orang), Married (62), Divorced (23).

3. **Attrition Berdasarkan Peran**

   * Highest: Laboratory Technician (49), Sales Executive (39), Research Scientist (38).
   * Terendah: Research Director (2).

4. **Perdepartemen**

   * Research & Development (107), Sales (66), Human Resources (6).

5. **Pengalaman Kerja**

   * Tenaga kerja terbaru (0–10 tahun) menunjukkan angka attrition tertinggi.

6. **Usia**

   * Kelompok 22–37 tahun paling rentan, menurun seiring usia.

7. **Pendapatan Bulanan**

   * Rentang \$2.500–\$5.000 memiliki attrition tertinggi (71 orang).

**Link Dashboard:** [[http://localhost:3000/public/dashboard/157bc3f7-874f-4ac9-95d7-cef041683f4f](http://localhost:3000/public/dashboard/157bc3f7-874f-4ac9-95d7-cef041683f4f)](http://127.0.0.1:3000/dashboard/2-datascience)

## Kesimpulan

Analisis menunjukkan bahwa lembur, status pernikahan, usia, pengalaman kerja, dan tingkat penghasilan berpengaruh signifikan terhadap attrition. Model prediktif berhasil diimplementasikan untuk memperkirakan risiko keluar karyawan.

## Rekomendasi Strategis

1. Menawarkan insentif atau mengurangi jam lembur bagi karyawan dengan beban kerja tinggi.
2. Program karier khusus untuk jabatan rentan seperti Laboratory Technician.
3. Menyesuaikan kebijakan gaji untuk kelompok berpenghasilan menengah ke bawah.
4. Pelatihan dan pengembangan bagi karyawan muda (<5 tahun pengalaman).
5. Pemanfaatan dashboard secara berkala untuk mendeteksi pola baru.
6. Survei kepuasan karyawan rutin untuk meningkatkan engagement.
