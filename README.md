# 📂 Aplikasi Arsip Surat Desa Karangduren

Aplikasi berbasis web untuk **mengarsipkan surat-surat resmi** Desa Karangduren, Kecamatan Pakisaji.  
Setiap surat resmi yang telah diterbitkan dapat dipindai (scan) dalam format **PDF**, lalu diunggah ke sistem agar dapat **disimpan, dicari, dan diunduh kembali** dengan mudah kapan saja.

---

## 🎯 Tujuan
Aplikasi ini dibuat untuk:
- Mempermudah **penyimpanan dan pengelolaan** surat resmi desa.
- Memberikan kemudahan bagi perangkat desa dalam **pencarian surat** berdasarkan judul atau kata kunci tertentu.
- Menyediakan akses **pengunduhan surat PDF** secara cepat dan terstruktur.

---

## ✨ Fitur Utama
- **Upload Surat (PDF)**  
  Petugas dapat mengunggah surat hasil pemindaian dalam format PDF.
- **Manajemen Arsip Surat**  
  Simpan informasi seperti **judul surat**, **nomor surat**, **tanggal terbit**, dan **keterangan**.
- **Pencarian Surat**  
  Cari arsip surat berdasarkan **judul** atau kata kunci secara cepat.
- **Pratinjau & Unduh Surat**  
  Lihat daftar surat yang tersimpan dan unduh file PDF sesuai kebutuhan.
- **Pengelolaan Data Admin**  
  Admin dapat menambah, mengedit, dan menghapus arsip surat sesuai hak akses.
- **Antarmuka Sederhana & Responsif**  
  Tampilan user-friendly dan dapat diakses dari komputer maupun perangkat mobile.

---

### 🖥️ CARA MENJALANKAN

Ikuti langkah-langkah berikut untuk menyiapkan dan menjalankan aplikasi **Aplikasi Arsip Surat Desa Karangduren** di lingkungan lokal:


#### 1️⃣ Kebutuhan Sistem
Pastikan sudah terpasang:
- **PHP 8.2+**
- **MySQL / MariaDB** *(atau sesuaikan `.env` bila menggunakan SQLite)*
- **Composer**
- **Laravel** 

#### 2️⃣ Persiapan Database (MySQL)
Jika database `aplikasiarsip` belum ada, buat terlebih dahulu:

- **Menggunakan file SQL**  
  Jalankan perintah berikut di terminal MySQL:
  ```sql
  SOURCE database/init/aplikasiarsip.sql;

- Atau buat manual
Jalankan perintah berikut:

  ```sql
  CREATE DATABASE IF NOT EXISTS si_arsip
  CHARACTER SET utf8mb4
  COLLATE utf8mb4_unicode_ci;

3️⃣ Konfigurasi File .env
- Salin file contoh:
  ```bash
  copy .env.example .env

- Sesuaikan variabel penting (contoh default Laragon/XAMPP):
  ```ini
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=aplikasiarsip
    DB_USERNAME=root
    DB_PASSWORD=

4️⃣ Migrasi & Seeder
- Jalankan migrasi dan seeder untuk membuat tabel dan menambahkan kategori default:

    ```bash
    php artisan migrate --seed
- Seeder akan menambahkan 4 kategori surat default:
    Undangan
    Pengumuman
    Nota Dinas
    Pemberitahuan

5️⃣ Storage Link
- Buat symbolic link untuk penyimpanan file:
    ```sql
    php artisan storage:link

6️⃣ Menjalankan Aplikasi
- Jalankan server Laravel:
    ```sql
    php artisan serve
- Atau langsung melalui browser :
  http://aplikasiarsip.test/about atau http://127.0.0.1:8000

---

## 🖼 Dokumentasi Visual Aplikasi

- Arsip Surat
<img width="1366" height="727" alt="image" src="https://github.com/user-attachments/assets/83366a03-cefd-4831-bcd5-97278fb515e8" />

- Arsip Surat >> Cari
<img width="1360" height="405" alt="image" src="https://github.com/user-attachments/assets/f8ca1292-0119-4d2a-818f-2861d48a310d" />

- Arsip Surat >> Arsipkan Surat
<img width="1363" height="589" alt="image" src="https://github.com/user-attachments/assets/1e365072-ae7b-4c75-a4a5-32ae08f6f0ff" />

- Arsip Surat >> Lihat
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/208ad03f-9033-42dd-85d6-9d29cfe762bd" />

- Arsip Surat >> Edit/Ganti File
<img width="1362" height="606" alt="image" src="https://github.com/user-attachments/assets/b55c4be2-f6fd-472a-ac13-ac14bd5e6963" />

- Arsip Surat >> Hapus
<img width="1362" height="547" alt="image" src="https://github.com/user-attachments/assets/ee299d96-402f-405e-b528-4f00a96184b9" />

- Kategori Surat
<img width="1366" height="567" alt="image" src="https://github.com/user-attachments/assets/54cddc02-8254-4d06-b1e3-25a5c2d30ebe" />

- Tambah Kategori Baru
<img width="1366" height="511" alt="image" src="https://github.com/user-attachments/assets/c4d37c1e-fea5-4a60-8df7-f21aace78ee7" />

- Kategori Surat >> Edit
<img width="1363" height="550" alt="image" src="https://github.com/user-attachments/assets/979959b0-4970-4a8d-8763-1fc05f847ff4" />

- Kategori Surat >> Hapus
<img width="1362" height="558" alt="image" src="https://github.com/user-attachments/assets/016e5c67-4c1b-4ca6-8d25-9ad1e99048e5" />

- Kategori Surat >> Cari
<img width="1363" height="367" alt="image" src="https://github.com/user-attachments/assets/d8c6b415-7576-49cc-9eca-4635a3f836c0" />

- About 
<img width="1363" height="416" alt="image" src="https://github.com/user-attachments/assets/19f2c025-6133-4a05-a61c-ca30f92f89b7" />

---

# Semoga Membantu ✌









