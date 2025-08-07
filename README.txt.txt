==================================================
ABSENSI QR CODE PEGAWAI - RRI SIBOLGA
==================================================

Deskripsi:
-----------
Aplikasi absensi online untuk pegawai RRI Sibolga yang menggunakan QR Code sebagai metode kehadiran individual. Setiap pegawai wajib memindai QR Code yang muncul di layar untuk membuka halaman absensi pribadi mereka dan memilih status kehadiran ("Hadir", "Sakit", atau "Tanpa Keterangan"). QR Code diperbarui secara otomatis setiap kali halaman direfresh untuk meningkatkan keamanan dan mencegah penyalahgunaan.

--------------------------------------------------
Fitur Utama:
-------------
- QR Code dinamis (unik setiap refresh), wajib dipindai oleh pegawai.
- Setiap QR Code berisi URL menuju halaman absensi personal pegawai.
- Tampilan daftar pegawai dalam bentuk grid hanya untuk admin/petugas.
- Admin dapat melihat status absensi seluruh pegawai secara real-time.
- Tombol "Hadir Semua" untuk kebutuhan khusus atau kondisi darurat.
- Data absensi dikirim langsung ke Google Spreadsheet.
- Tanggal & waktu real-time ditampilkan di atas halaman.
- Desain modern, responsif, dan ramah pengguna.
- Header dan logo resmi "RRI Sibolga" tampil di bagian atas halaman.

--------------------------------------------------
Cara Menggunakan (Admin):
--------------------------
1. Buka file `index.html` di browser komputer admin.
2. Arahkan pegawai untuk memindai QR Code yang tampil di layar menggunakan ponsel mereka.
3. Setiap pegawai akan dibawa ke halaman absensi pribadi (via URL dari QR Code).
4. Pegawai memilih status: Hadir, Sakit, atau Tanpa Keterangan.
5. Setelah memilih, data akan dikirim ke Spreadsheet Google secara otomatis.
6. Admin dapat meninjau data yang masuk dari Spreadsheet.

--------------------------------------------------
Cara Menggunakan (Pegawai):
----------------------------
1. Pindai QR Code yang tampil di layar admin menggunakan kamera atau aplikasi QR scanner.
2. Isi atau konfirmasi data diri (opsional, tergantung sistem).
3. Pilih status kehadiran.
4. Tunggu notifikasi bahwa data berhasil dikirim.

--------------------------------------------------
Konfigurasi Google Spreadsheet:
-------------------------------
1. Buat Google Spreadsheet dengan nama: Absensi RRI Sibolga.
2. Tambahkan kolom di baris pertama:
   - A1: Tanggal Waktu
   - B1: Nama Pegawai
   - C1: Status
   - (opsional kolom tambahan: Lokasi, Perangkat, dsb.)
3. Buat Google Apps Script dan tempel kode backend dari dokumentasi.
4. Ganti SPREADSHEET_ID di dalam script dengan ID spreadsheet Anda.
5. Deploy script sebagai Web App:
   - Execute as: Me
   - Access: Anyone
6. Salin URL Web App.
7. Di `index.html`, ganti:
   fetch("https://script.google.com/macros/s/YOUR_SCRIPT_ID/exec", ...)
   dengan URL Web App Anda.

--------------------------------------------------
Struktur Folder:
-----------------
/absensi-rri
├── index.html         → Halaman utama & generator QR Code
├── README.txt         → Petunjuk penggunaan & konfigurasi
├── (opsional) absensi.html → Halaman yang diakses setelah scan QR

--------------------------------------------------
Catatan Tambahan:
------------------
- QR Code harus dipindai oleh setiap pegawai untuk absen.
- Pastikan perangkat pegawai memiliki koneksi internet aktif.
- Jangan gunakan QR Code yang sama dua kali — selalu refresh halaman untuk keamanan.
- Gunakan browser terbaru untuk hasil terbaik.

--------------------------------------------------
Dibuat untuk:
-------------
RRI Sibolga
Agustus 2025

Developer:
[Citra priadi pasaribu S.IP]
[priadipasaribu@gmai.com]
