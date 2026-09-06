# Management Library (Manajemen Perpustakaan Sederhana)

Sebuah aplikasi manajemen perpustakaan sederhana dibangun dengan Laravel 10 untuk kebutuhan pengelolaan koleksi buku, peminjaman, dan anggota. Cocok sebagai proyek demo, tugas akhir, atau basis yang bisa dikembangkan untuk sistem perpustakaan kecil sampai menengah.

---

## Ringkasan singkat
Aplikasi ini adalah skeleton Laravel yang sudah disiapkan untuk fitur manajemen perpustakaan: operasi CRUD pada buku dan anggota, proses peminjaman/pengembalian, serta antarmuka berbasis Vite. Target pengguna: pengembang yang ingin menjalankan atau mengembangkan sistem manajemen perpustakaan berbasis Laravel.

### Stack
- Language(s): PHP (Laravel) dan JavaScript (Vite)
- Framework / runtime: Laravel 10 + Vite (asset bundling)
- Notable libraries (dari composer.json):
  - laravel/framework (^10.10)
  - laravel/sanctum (auth / API token)
  - realrashid/sweet-alert (alert UI)
  - guzzlehttp/guzzle (HTTP client)
  - PHPUnit, Faker (testing & seeding)

License: MIT (lihat composer.json)

---

## Struktur top-level (apa yang ada di repo)
Berikut file/entri top-level yang ada sekarang:
- .editorconfig
- .env
- .env.example
- README.md
- artisan
- composer.json
- composer.lock
- package.json
- package-lock.json
- phpunit.xml
- vite.config.js

Catatan: composer.json mengarahkan autoload ke direktori `app/`, `database/factories/`, `database/seeders/` dan `tests/`, sehingga kode aplikasi normalnya berada di direktori tersebut (jika belum muncul di repo, pastikan semua file/direktori proyek dilacak di Git).

**Bagaimana bagian-bagian bekerja bersama:**  
Aplikasi adalah Laravel monolitik: request → route → controller (app/) → model (Eloquent) → views atau API. Asset front-end dikelola via Vite (package.json + vite.config.js).

---

## Fitur (yang biasanya diharapkan dari project ini)
- Autentikasi / otorisasi dasar (Laravel Sanctum tersedia untuk API)
- CRUD Buku (title, author, isbn, stok, dst.)
- CRUD Anggota
- Proses Peminjaman & Pengembalian
- Notifikasi sederhana / alert UI (SweetAlert)
- Seeder & Factory untuk data contoh (faker)

(Implementasi aktual fitur bergantung pada isi folder `app/`/`routes/`/`database/` — jika belum ada, fitur ini adalah blueprint yang perlu diimplementasikan.)

---

## Persyaratan
- PHP >= 8.1
- Composer
- MySQL atau MariaDB (sesuaikan DB_* di .env)
- Node.js & npm (untuk asset, Vite)
- (Opsional) Docker & Laravel Sail jika ingin menjalankan container

---

## Cara menjalankan (dari clone kosong → lokal)
Jalankan perintah berikut di terminal:

1. Clone repo
   ```bash
   git clone https://github.com/fadhilarahmadani/management-library.git
   cd management-library