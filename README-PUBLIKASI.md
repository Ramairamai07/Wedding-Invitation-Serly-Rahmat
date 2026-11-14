# Website Pernikahan Serly & Rahmat

Paket website undangan statis yang siap diunggah ke GitHub Pages. Desain mempertahankan nuansa Jawa modern dengan palet maroon, krem, dan emas.

## Isi paket
- `index.html` — halaman utama undangan.
- `assets/` — enam foto yang sudah dioptimalkan ke format WebP.
- `supabase-setup.sql` — struktur tabel dan kebijakan keamanan RSVP serta ucapan.

## Informasi undangan yang saat ini digunakan
- Mempelai: Serly Karina Sari & Rahmat Ramadhan.
- Hari/tanggal: Sabtu, 24 April 2027.
- Akad: 08.00–10.00 WIB.
- Resepsi: 11.00–14.00 WIB.
- Lokasi: Hotel Grand Palace, Jl. Ade Irma Suryani No. 23, Kasin, Klojen, Kota Malang, Jawa Timur.
- Peta: tautan Google Maps yang sudah ada pada file HTML.

Mohon cek kembali semua informasi acara sebelum membagikan tautan publik.

## Publikasi gratis melalui GitHub Pages
1. Masuk ke GitHub dan buat repository baru, misalnya `undangan-serly-rahmat`.
2. Ekstrak ZIP ini di komputer.
3. Unggah **isi folder** paket (bukan folder pembungkusnya) ke root repository. Pastikan `index.html`, `supabase-setup.sql`, `README-PUBLIKASI.md`, dan folder `assets` berada di tingkat teratas.
4. Buka **Settings → Pages** pada repository.
5. Pada **Build and deployment**, pilih **Deploy from a branch**.
6. Pilih branch `main` dan folder `/(root)`, lalu klik **Save**.
7. Tunggu proses deployment selesai. URL umumnya berbentuk `https://USERNAME.github.io/undangan-serly-rahmat/`.

## Mengaktifkan RSVP dan ucapan bersama (opsional, gratis sesuai kuota Supabase)
Website dapat dibuka tanpa database, tetapi formulir RSVP dan ucapan belum menyimpan data bersama sampai Supabase dikonfigurasi.

1. Buat project di Supabase.
2. Buka **SQL Editor**, jalankan isi `supabase-setup.sql`.
3. Buka **Project Settings → API** dan salin Project URL serta anon/publishable key.
4. Buka `index.html`, cari `KONFIGURASI DATABASE (Supabase)` di bagian script.
5. Isi nilai `SUPABASE_URL` dan `SUPABASE_ANON_KEY` dengan data project Anda.
6. Simpan, unggah ulang `index.html` ke GitHub, lalu uji RSVP dan ucapan.

**Keamanan:** gunakan hanya anon/publishable key di browser. Jangan pernah memasukkan `service_role` key, password, atau kredensial admin ke HTML maupun repository publik. SQL mengaktifkan Row Level Security; pengunjung dapat mengirim RSVP dan ucapan, tetapi tidak dapat membaca daftar RSVP. Ucapan dapat dibaca publik.

## Pemeriksaan sebelum membagikan
- Buka URL GitHub Pages dari ponsel dan komputer.
- Coba tombol Buka Undangan, countdown, Simpan Tanggal, dan Google Maps.
- Pastikan seluruh foto muncul (folder `assets` harus ikut diunggah).
- Uji RSVP/ucapan setelah Supabase dihubungkan.
- Jangan unggah nomor rekening, alamat pribadi, QRIS, atau tautan siaran langsung yang belum final.

## Catatan
Paket ini menyiapkan website untuk GitHub Pages. Saya tidak dapat masuk ke akun GitHub Anda atau melakukan deployment tanpa akses dan persetujuan akun; langkah publikasi di atas dilakukan dari akun Anda.
