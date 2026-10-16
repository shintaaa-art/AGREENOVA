# AGREENOVA — Prototype Website

Website prototype bertema pertanian dengan HTML, CSS, dan JavaScript murni. Tidak membutuhkan framework, Node.js, database, atau API berbayar.

## Fitur
- Beranda responsif dengan navigasi satu halaman.
- Katalog pupuk dengan pencarian, filter kategori, dan pengurutan harga/stok.
- Informasi stok dan harga indikatif.
- Tentang AGREENOVA dan form kontak yang membuka aplikasi email (mailto).
- Dashboard admin demo: tambah, edit, hapus produk, pulihkan data awal, dan ekspor CSV.
- Perubahan katalog disimpan pada `localStorage` browser yang sedang dipakai.
- Ilustrasi lokal disimpan di folder `assets`.

## Struktur folder

```text
agreenova/
├── index.html
├── styles.css
├── app.js
├── README.md
├── vercel.json
└── assets/
    ├── favicon.svg
    ├── farm.svg
    └── field.svg
```

## Jalankan secara lokal

**Cara cepat:** buka `index.html` di browser.

**Cara disarankan:**
1. Pasang Visual Studio Code.
2. Buka folder `agreenova` di VS Code (`File > Open Folder`).
3. Pasang ekstensi **Live Server** dari Marketplace VS Code (opsional).
4. Klik kanan `index.html` → **Open with Live Server**.
5. Website terbuka di browser. Edit file lalu simpan untuk melihat perubahan.

Website ini tidak membutuhkan `npm install` atau proses build.

## Cara deploy ke GitHub dan Vercel

1. Buat repository baru di GitHub, misalnya `agreenova`.
2. Upload seluruh isi folder ini ke root repository (pastikan `index.html` berada di root, bukan di folder bersarang).
3. Buka Vercel dan masuk menggunakan GitHub.
4. Pilih **Add New → Project**, lalu impor repository `agreenova`.
5. Untuk proyek HTML statis ini, gunakan konfigurasi tanpa framework. Biarkan Build Command kosong dan Output Directory sesuai root/default. Jika diminta, gunakan `.` sebagai Output Directory.
6. Klik **Deploy** dan tunggu hingga selesai. Vercel akan memberikan URL `*.vercel.app`.
7. Setelah perubahan didorong ke branch yang terhubung, Vercel dapat melakukan deployment ulang secara otomatis.

File `vercel.json` mengatur fallback halaman agar rute tidak dikenal kembali ke `index.html`.

## Catatan penting tentang prototype

- Nama produk, harga, dan jumlah stok di katalog adalah **data ilustrasi**, bukan penawaran resmi atau data stok pupuk subsidi pemerintah.
- Dashboard admin tidak memiliki autentikasi. Jangan gunakan untuk data bisnis sensitif atau sebagai dashboard admin produksi.
- `localStorage` hanya tersimpan di browser/perangkat yang sama. Perubahan admin tidak otomatis terlihat di perangkat lain dan tidak tersimpan ke server.
- Form kontak menggunakan `mailto:`. Pesan tidak dikirim otomatis dan membutuhkan aplikasi email yang terkonfigurasi.
- Tidak ada sistem pembayaran, pemesanan online sungguhan, sinkronisasi stok, atau akun pengguna.
- Domain khusus opsional; URL `vercel.app` sudah cukup untuk demo publik. Periksa ketentuan paket Vercel Hobby terbaru dan pastikan penggunaan sesuai ketentuan mereka.

## Kustomisasi cepat
- Ubah warna utama di bagian `:root` pada `styles.css`.
- Ubah produk awal di konstanta `INITIAL_PRODUCTS` pada `app.js`.
- Ubah teks beranda dan bagian lain di `index.html`.
