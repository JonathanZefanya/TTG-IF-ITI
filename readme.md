Tentu! Berikut adalah versi yang telah diperbaiki dan dirapikan dari README kamu, dengan penulisan yang lebih konsisten dan profesional:

---

# 🌐 Web Tools – All-in-One Online Tools Website

[🔗 Lihat Website](https://s.zyrex.win)

**Web Tools** adalah website all-in-one yang menyediakan berbagai alat online bermanfaat seperti pemendek URL, generator QR code, tautan dinamis, tautan acara, serta lebih dari 100+ tools web lainnya. Website ini dibangun menggunakan PHP dan berjalan di atas stack teknologi yang ringan namun powerful.

---

## 🚀 Demo

Klik tautan berikut untuk melihat demo secara langsung:

👉 [https://s.zyrex.win](https://s.zyrex.win)

---

## 🛠️ Teknologi yang Digunakan

- **Bahasa Pemrograman**: PHP 8.2.4  
- **Web Server**: Apache (XAMPP)  
- **Database**: MySQL 5.7.3+ atau MariaDB  
- **Ekstensi PHP**:
  - `cURL`
  - `OpenSSL`
  - `mbstring`
  - `MySQLi`

---

## 📄 Dokumentasi Instalasi Manual

### 1. Persyaratan Server

- **PHP versi 8.1 atau lebih tinggi** (project ini menggunakan PHP 8.2.4)
- **MySQL 5.7.3+ atau MariaDB**
- Apache Web Server atau yang kompatibel
- Ekstensi PHP yang dibutuhkan:
  - `cURL`
  - `OpenSSL`
  - `mbstring`
  - `MySQLi`
- Modul `.htaccess` harus aktif

### 2. Langkah Instalasi

1. **Clone atau download repository**
   ```bash
   git clone https://github.com/JonathanZefanya/TTG-IF-ITI.git
   ```

2. **Pindahkan ke folder `htdocs`** (jika menggunakan XAMPP)
   ```bash
   mv web-tools /path-to-xampp/htdocs/
   ```

3. **Buat database baru**
   - Buka `phpMyAdmin`
   - Buat database baru, misalnya: `web-tools`

4. **Import file SQL**
   - Import file `database/dump.sql` ke database yang baru dibuat

5. **Konfigurasi database**
   - Edit file `config.php` dan sesuaikan dengan konfigurasi lokal:
     ```php
     define('DATABASE_SERVER',   'localhost');
     define('DATABASE_USERNAME', 'root');
     define('DATABASE_PASSWORD', 'root');
     define('DATABASE_NAME',     'web-tools');
     define('SITE_URL',          'http://localhost/web-tools/');
     ```

6. **Akses website**
   - Buka browser dan akses:
     ```
     http://localhost/web-tools/
     ```

---

## 📚 Fitur Utama

- ✅ URL Shortener  
- ✅ Dynamic Links & Files  
- ✅ QR Code Generator  
- ✅ Contact & Event Links  
- ✅ 100+ Web Tools siap pakai  
- ✅ Admin Panel  
- ✅ Statistik & Analytics

---

## 📬 Kontak

Jika ada pertanyaan, saran, atau bug yang ingin dilaporkan, silakan hubungi melalui halaman kontak di website atau melalui email pengembang.

---

## 📎 Lisensi

Proyek ini bersifat **private** dan hanya untuk penggunaan pribadi. Dilarang mendistribusikan ulang tanpa izin.

---

Kalau kamu ingin, aku bisa bantu tambahkan badge GitHub (jika tersedia), fitur CI/CD, atau instruksi deploy ke hosting juga. Mau sekalian dibikin versi dalam bahasa Inggris juga?