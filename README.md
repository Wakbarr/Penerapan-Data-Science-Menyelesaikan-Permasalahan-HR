# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

**Terakhir diperbarui pada: Senin, 16 Juni 2025, 15:09 WIB**

## Business Understanding

Jaya Jaya Maju adalah perusahaan multinasional yang berdiri sejak tahun 2000 dan memiliki lebih dari 1.000 karyawan di berbagai wilayah. Perusahaan ini bergerak di berbagai sektor dengan fokus utama pada pengembangan sumber daya manusia dan teknologi. Meskipun telah berkembang pesat, Jaya Jaya Maju menghadapi tantangan signifikan terkait tingginya tingkat *attrition* (pergantian karyawan) yang melebihi 10%. Kondisi ini dapat meningkatkan biaya rekrutmen, menurunkan produktivitas, dan mengganggu stabilitas organisasi.

## Permasalahan Bisnis

1. **Faktor Penyebab Attrition Tinggi**  
   Perusahaan perlu menentukan variabel apa saja yang paling berpengaruh terhadap keputusan karyawan untuk keluar dari perusahaan.

2. **Desain Visualisasi Data yang Efektif**  
   Tim HR membutuhkan grafik dan laporan yang mudah dipahami untuk memantau metrik utama secara *real-time*.

3. **Proyeksi Risiko Keluar Karyawan**  
   Perusahaan ingin membangun model prediktif untuk mengidentifikasi karyawan yang berpotensi meninggalkan perusahaan, sehingga dapat dilakukan intervensi lebih awal.

## Cakupan Proyek

1. **Analisis Data Karyawan**  
   - Melakukan eksplorasi data untuk menemukan pola dan *insight* terkait *attrition*.  
   - Mengidentifikasi fitur paling krusial yang berkaitan dengan keputusan karyawan untuk resign.

2. **Pembuatan Dashboard Bisnis**  
   - Menyajikan tampilan interaktif untuk memonitor faktor-faktor kunci *attrition*.  
   - Menyediakan panel kontrol bagi manajer HR untuk pengambilan keputusan berbasis data.

3. **Pengembangan Model Prediksi**  
   - Melatih model *machine learning* untuk memperkirakan potensi *attrition* tiap individu.  
   - Memprioritaskan tindakan pencegahan bagi karyawan berisiko tinggi.

4. **Rekomendasi dan Tindak Lanjut**  
   - Memberikan saran strategi HR berdasarkan hasil analisis dan prediksi.

## Persiapan

### Sumber Data
Dataset karyawan berisi informasi lengkap mengenai demografis, pengalaman kerja, kompensasi, dan departemen. Data dapat diakses di:  
[https://github.com/dicodingacademy/dicoding_dataset/blob/main/employee/employee_data.csv](https://github.com/dicodingacademy/dicoding_dataset/blob/main/employee/employee_data.csv)

### Setup Environment

Untuk memastikan proyek dapat dijalankan dengan lancar, ikuti langkah-langkah berikut secara sistematis:

1. **Membuat dan Mengaktifkan Virtual Environment (venv)**  
   Virtual environment digunakan untuk mengisolasi lingkungan pengembangan agar dependensi proyek tidak bertabrakan dengan sistem utama. Berikut langkah-langkahnya:  
   - Pastikan Python 3.9 sudah terinstal di sistem Anda.  
   - Buat virtual environment dengan perintah:  
     ```bash
     python -m venv hr_project
     ```
   - Aktifkan virtual environment:  
     - Pada Windows:  
       ```bash
       hr_project\Scripts\activate
       ```
     - Pada macOS/Linux:  
       ```bash
       source hr_project/bin/activate
       ```
   - Setelah diaktifkan, Anda akan melihat `(hr_project)` di terminal, menandakan virtual environment aktif.

2. **Menginstal Dependensi dari `requirements.txt`**  
   Proyek ini membutuhkan beberapa pustaka Python seperti Pandas, Scikit-learn, dan SQLAlchemy. Pastikan file `requirements.txt` tersedia di direktori proyek, lalu instal dependensi dengan perintah:  
   ```bash
   pip install -r requirements.txt
   ```
   Perintah ini akan menginstal semua pustaka yang diperlukan untuk menjalankan proyek.

3. **Menyiapkan Metabase**  
   - Metabase digunakan untuk visualisasi data dan dijalankan melalui Docker pada port `3000`. Pastikan Docker sudah terinstal.  
   - Jalankan perintah berikut untuk menjalankan Metabase:  
     ```bash
     docker run -d -p 3000:3000 metabase/metabase
     ```
   - Setelah Metabase berjalan, akses melalui browser di `http://localhost:3000` dan sambungkan ke database Supabase.

4. **Cara Menjalankan Skrip Python (.py)**  
   File utama proyek ini adalah `main.py`, yang berisi kode untuk analisis data, pelatihan model, dan pembuatan laporan. Untuk menjalankannya:  
   - Pastikan virtual environment sudah aktif.  
   - Jalankan skrip dengan perintah:  
     ```bash
     python main.py
     ```
   - Jika ada parameter tambahan, misalnya untuk menentukan lokasi dataset, gunakan:  
     ```bash
     python main.py --dataset employee_data.csv
     ```

5. **Langkah Awal Tambahan**  
   - Clone repository proyek:  
     ```bash
     git clone <URL_REPOSITORY_PROYEK>
     ```
   - Pastikan semua dependensi terinstal dan Metabase telah tersambung dengan database.

## Business Dashboard

Dashboard interaktif telah dibuat untuk membantu tim HR memantau metrik *attrition* secara *real-time*. Berikut rincian komponen dashboard:

1. **Tinjauan Umum**  
   - **Total Karyawan:** 1.058 orang.  
   - **Jumlah Attrition:** 179 orang.  
   - **Persentase Attrition:** 16,92% dari total karyawan.

2. **Faktor-Faktor Kunci**  
   - **Overtime:** 54,7% karyawan yang lembur memilih resign.  
   - **Status Pernikahan:** Single (94 orang), Married (62 orang), Divorced (23 orang).

3. **Attrition Berdasarkan Peran**  
   - Tertinggi: Laboratory Technician (49 orang), Sales Executive (39 orang), Research Scientist (38 orang).  
   - Terendah: Research Director (2 orang).

4. **Per Departemen**  
   - Research & Development: 107 orang.  
   - Sales: 66 orang.  
   - Human Resources: 6 orang.

5. **Pengalaman Kerja**  
   - Karyawan dengan pengalaman 0–10 tahun menunjukkan angka *attrition* tertinggi.

6. **Usia**  
   - Kelompok usia 22–37 tahun paling rentan untuk resign, dengan tren menurun seiring bertambahnya usia.

7. **Pendapatan Bulanan**  
   - Rentang pendapatan $2.500–$5.000 memiliki angka *attrition* tertinggi (71 orang).

**Link Dashboard:**  
[http://localhost:3000/public/dashboard/157bc3f7-874f-4ac9-95d7-cef041683f4f](http://localhost:3000/public/dashboard/157bc3f7-874f-4ac9-95d7-cef041683f4f)

**Akses Dashboard:**  
Dashboard ini dapat diakses dengan kredensial berikut:  
- URL: `http://localhost:3000`  
- Username: `root@mail.com`  
- Password: `root123`

## Conclusion

Analisis menunjukkan bahwa faktor-faktor seperti lembur, status pernikahan, usia, pengalaman kerja, dan tingkat penghasilan memiliki pengaruh signifikan terhadap tingkat *attrition*. Model prediktif yang dikembangkan berhasil mengidentifikasi karyawan dengan risiko tinggi untuk keluar, memungkinkan intervensi dini oleh tim HR. Dashboard yang dibuat memberikan gambaran yang jelas dan interaktif untuk mendukung pengambilan keputusan berbasis data.

## Rekomendasi Action Items

1. **Mengurangi Beban Lembur**  
   Menawarkan insentif atau mengurangi jam lembur bagi karyawan dengan beban kerja tinggi untuk mencegah kelelahan dan meningkatkan retensi.

2. **Program Karier untuk Jabatan Rentan**  
   Membuat program pengembangan karier khusus untuk jabatan dengan *attrition* tinggi, seperti Laboratory Technician.

3. **Penyesuaian Kebijakan Gaji**  
   Menyesuaikan gaji untuk kelompok berpenghasilan menengah ke bawah (rentang $2.500–$5.000) agar lebih kompetitif.

4. **Pelatihan untuk Karyawan Muda**  
   Menyediakan pelatihan dan pengembangan bagi karyawan dengan pengalaman kurang dari 5 tahun untuk meningkatkan keterikatan mereka.

5. **Pemantauan Berkala via Dashboard**  
   Memanfaatkan dashboard secara rutin untuk mendeteksi pola *attrition* baru dan merespons dengan cepat.

6. **Survei Kepuasan Karyawan**  
   Melakukan survei kepuasan karyawan secara rutin untuk memahami kebutuhan mereka dan meningkatkan *engagement*.
