
# Warehouse Inventory Management System

## 1. Deskripsi Aplikasi

Warehouse Inventory Management System merupakan aplikasi berbasis web yang dikembangkan untuk membantu pengelolaan persediaan barang pada gudang.

Aplikasi ini memudahkan administrator dalam mengelola data barang, kategori, supplier, transaksi barang masuk, transaksi barang keluar, serta memantau jumlah persediaan secara terstruktur.

## 2. Tujuan Aplikasi

- Mempermudah pengelolaan data persediaan barang.
- Memantau jumlah stok barang secara aktual.
- Mencatat transaksi barang masuk dan barang keluar.
- Mengurangi risiko kesalahan pencatatan stok.
- Menyediakan laporan persediaan dan riwayat transaksi.

## 3. Teknologi yang Digunakan

- Framework: Laravel 12
- Bahasa pemrograman: PHP
- Database: MySQL
- Frontend: HTML, CSS, Bootstrap, Blade
- JavaScript: Chart.js
- Web server lokal: Laragon
- Code editor: Visual Studio Code

## 4. Fitur Aplikasi

### A. Autentikasi
- Login administrator.
- Logout administrator.
- Pembatasan akses halaman menggunakan autentikasi.

### B. Dashboard
- Menampilkan jumlah produk.
- Menampilkan jumlah kategori dan supplier.
- Menampilkan total stok barang.
- Menampilkan ringkasan transaksi.
- Menampilkan grafik transaksi.
- Menampilkan peringatan stok menipis.
- Menampilkan aktivitas transaksi terbaru.

### C. Manajemen Kategori
- Menambahkan kategori barang.
- Mengubah data kategori.
- Menghapus kategori.

### D. Manajemen Supplier
- Menambahkan data supplier.
- Mengubah data supplier.
- Menghapus data supplier.

### E. Manajemen Produk
- Menambahkan data produk.
- Mengubah informasi produk.
- Menghapus produk.
- Menghubungkan produk dengan kategori dan supplier.

### F. Transaksi Barang Masuk
- Mencatat barang masuk.
- Menentukan jumlah dan tanggal transaksi.
- Memperbarui stok secara otomatis.

### G. Transaksi Barang Keluar
- Mencatat barang keluar.
- Memvalidasi ketersediaan stok.
- Mengurangi stok secara otomatis.
- Menolak transaksi apabila stok tidak mencukupi.

### H. Laporan
- Laporan persediaan barang.
- Laporan barang masuk.
- Laporan barang keluar.
- Filter laporan berdasarkan tanggal.

## 5. Persyaratan Sistem

- PHP 8.2 atau lebih baru.
- Composer.
- Node.js dan NPM.
- MySQL.
- Laragon atau web server yang mendukung Laravel.
- Browser modern.

## 6. Cara Instalasi

1. Salin folder project ke direktori web server.
2. Buka terminal pada folder project.
3. Jalankan perintah:

```bash
composer install
```

4. Salin file konfigurasi:

```bash
copy .env.example .env
```

5. Buat database MySQL dengan nama:

```text
warehouse_inventory
```

6. Sesuaikan konfigurasi database pada file `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=warehouse_inventory
DB_USERNAME=root
DB_PASSWORD=
```

7. Generate application key:

```bash
php artisan key:generate
```

8. Jalankan migrasi database:

```bash
php artisan migrate
```

9. Install dependency frontend:

```bash
npm install
```

10. Jalankan aplikasi:

```bash
php artisan serve
```

11. Buka browser dan akses:

```text
http://127.0.0.1:8000
```

## 7. Database

Database yang digunakan bernama `warehouse_inventory`, dengan tabel utama:

- users
- categories
- suppliers
- products
- stock_ins
- stock_outs

Database juga memiliki tabel pendukung bawaan Laravel untuk cache dan queue.

## 8. Pengguna Aplikasi

Aplikasi menggunakan autentikasi administrator untuk mengakses fitur pengelolaan persediaan.

Akun administrator dibuat melalui proses konfigurasi awal aplikasi.

## 9. Penutup

Warehouse Inventory Management System diharapkan dapat membantu proses pengelolaan persediaan barang menjadi lebih efektif, terstruktur, dan akurat melalui sistem informasi berbasis web.
