## 🚀 Deploy ke cPanel (Shared Hosting)
---

### 📁 1. Struktur Direktori

Pastikan struktur project kamu seperti ini sebelum upload:

```
web-tools/
├── config.php
├── index.php
├── database/
│   └── dump.sql
├── assets/
├── includes/
└── ...
```

---

### ☁️ 2. Upload ke cPanel

1. **Zip seluruh folder `web-tools`**
2. Masuk ke **cPanel > File Manager**
3. Masuk ke folder `public_html/`
4. Upload file `.zip` tadi dan **extract**
5. Pastikan file seperti `index.php`, `config.php`, dan lainnya berada langsung di dalam `public_html/`, **bukan** di subfolder seperti `public_html/web-tools/`

---

### 🛠️ 3. Buat Database di cPanel

1. Masuk ke **MySQL® Databases** di cPanel
2. **Buat database** baru, misalnya `yourcpanel_webtools`
3. **Buat user database** dan beri akses penuh ke database tadi
4. Simpan informasi:
   - DB Name
   - DB User
   - DB Password

---

### 🧩 4. Import SQL

1. Masuk ke **phpMyAdmin** dari cPanel
2. Pilih database yang barusan dibuat
3. Import file `dump.sql` dari folder `database/`

---

### ⚙️ 5. Konfigurasi `config.php`

Edit file `config.php` agar cocok dengan pengaturan di cPanel:

```php
define('DATABASE_SERVER',   'localhost');
define('DATABASE_USERNAME', 'your_db_user');
define('DATABASE_PASSWORD', 'your_db_password');
define('DATABASE_NAME',     'your_db_name');
define('SITE_URL',          'https://yourdomain.com/');
```

---

### 🔐 6. Cek `.htaccess`

Pastikan file `.htaccess` sudah ada di root dan tidak terhapus saat upload ZIP. Contoh isi dasar:

```apache
Options -Indexes

RewriteEngine On

RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-l

RewriteRule ^(.+)$ index.php?altum=$1 [QSA,L]

<IfModule mod_expires.c>
    <filesMatch ".(gif|ico|jpg|jpeg|png|svg|webp)$">
        Header set Cache-Control "max-age=31536000, public"
    </filesMatch>

    <filesMatch ".(js|css)$">
        Header set Cache-Control "max-age=31536000, public"
    </filesMatch>
</IfModule>

<IfModule mod_headers.c>
    <Files ~ "sw\.js">
        Header set Service-Worker-Allowed: /
    </Files>
</IfModule>
```

Kalau menggunakan subdomain atau subfolder, bisa disesuaikan.

---

### ✅ 7. Selesai!

Buka domain kamu, misalnya `https://yourdomain.com/` dan project seharusnya sudah jalan.

---