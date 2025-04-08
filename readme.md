# 🌐 Web Tools – All-in-One Online Tools Website

[🔗 Lihat Website](https://s.zyrex.win)

**Web Tools** adalah website all-in-one yang menyediakan berbagai alat online bermanfaat seperti pemendek URL, QR code generator, dynamic files, event links, dan lebih dari 100+ tools web lainnya. Website ini dibuat menggunakan PHP dan berjalan di atas stack teknologi yang ringan namun powerful.

---

## 🚀 Demo

Klik link berikut untuk melihat demo langsung:

👉 [https://s.zyrex.win](https://s.zyrex.win)

---

## 🛠️ Teknologi yang Digunakan

- **Bahasa Pemrograman**: PHP 8.2.4
- **Web Server**: Apache (XAMPP)
- **Database**: MySQL 5.7.3+ atau MariaDB equivalent
- **PHP Extensions**:
  - `cURL`
  - `OpenSSL`
  - `mbstring`
  - `MySQLi`

---

## 📄 Dokumentasi Instalasi Manual

### 1. Persyaratan Server

- **PHP Versi 8.1 atau lebih tinggi** (Project ini menggunakan PHP 8.2.4)
- **MySQL 5.7.3+ atau MariaDB**
- Apache Web Server atau server lain yang kompatibel
- Ekstensi PHP yang wajib:
  - `cURL`
  - `OpenSSL`
  - `mbstring`
  - `MySQLi`
- Modul `.htaccess` harus aktif di server

### 2. Langkah Instalasi

1. **Clone atau Download Repository**
   ```bash
   git clone <repository-url>
   ```

2. **Pindahkan ke folder htdocs** (jika menggunakan XAMPP)
   ```bash
   mv web-tools /path-to-xampp/htdocs/
   ```

3. **Buat Database Baru**
   - Buka `phpMyAdmin`
   - Buat database baru, misal `web-tools`

4. **Import File SQL**
   - Import file `database/dump.sql` yang ada di dalam folder proyek ke database yang baru dibuat.

5. **Konfigurasi Database**
   - Edit file `config.php` dan sesuaikan:
     ```
    define('DATABASE_SERVER',   'localhost');
    define('DATABASE_USERNAME', 'root');
    define('DATABASE_PASSWORD', 'root');
    define('DATABASE_NAME',     'web-tools');
    define('SITE_URL',          'http://localhost/Latihan-Web/Web-Tools/');
     ```

6. **Akses Website**
   - Buka browser dan akses:
     ```
     http://localhost/web-tools/
     ```

---

## 📚 Fitur Utama

- ✅ URL Shortener
- ✅ Dynamic Link & Files
- ✅ QR Code Generator
- ✅ Contact & Event Links
- ✅ 100+ Web Tools Siap Pakai
- ✅ Admin Panel
- ✅ Statistik & Analytics

---

## 📬 Kontak

Jika ada pertanyaan atau bug yang ingin dilaporkan, silakan hubungi melalui halaman kontak di dalam website atau melalui email pengembang.

---

## 📎 License

Project ini bersifat private untuk penggunaan pribadi. Dilarang mendistribusikan ulang tanpa izin.

```