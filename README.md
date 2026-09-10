# Benang Scale Monitor

Website untuk membaca berat dari timbangan RS-232 (lewat port COM/USB) dan
otomatis mengecek apakah sisa benang masih bisa dipakai, berdasarkan tabel
referensi 16 jenis benang.

Dibuka lewat browser **Chrome** atau **Edge** (karena memakai Web Serial API).

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub (public), misalnya `benang-scale-monitor`.
2. Di komputer kamu, buka terminal di folder ini lalu jalankan:

   ```bash
   git remote add origin https://github.com/USERNAME/benang-scale-monitor.git
   git branch -M main
   git commit -m "Initial commit: benang scale monitor"
   git push -u origin main
   ```

   Ganti `USERNAME` dengan username GitHub kamu.

3. Di GitHub, buka repo tersebut → **Settings** → **Pages**.
4. Pada **Source**, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
5. Tunggu 1–2 menit, GitHub akan memberi URL seperti:

   ```
   https://USERNAME.github.io/benang-scale-monitor/
   ```

6. Buka URL itu lewat **Chrome/Edge** di komputer yang tersambung ke
   timbangan. Karena diakses lewat `https://`, Web Serial API akan berfungsi
   normal (tidak perlu server lokal lagi).

## Catatan

- Web Serial API butuh koneksi `https://` atau `http://localhost` — GitHub
  Pages otomatis pakai `https://`, jadi sudah memenuhi syarat.
- Sesuaikan baud rate, parity, dan pola regex berat di panel kiri sesuai
  format output timbangan kamu.
- Semua data timbang bersifat lokal di browser — tidak ada data yang dikirim
  ke server manapun.
