# Mini Project Struk Kasir

## Identitas
Nama: MUHAMMAD HANAFI NASUTION
NIM: 25110057
Kelas: TK D SIANG
Mata kuliah: Praktik Pemrograman WEB II
Pertemuan: 6

## Lingkungan
- XAMPP
- Versi PHP: PHP_VERSION
- Visual Studio Code
- Browser:

## Cara Menjalankan
1. Letakkan folder proyek di htdocs XAMPP.
2. Jalankan Apache melalui XAMPP Control Panel.
3. Buka URL proyek melalui browser.

URL proyek:
http://localhost/kasir_p06_nama/

## Struktur Berkas
- cek.php: pemeriksaan versi PHP
- helpers.php: fungsi perhitungan dan format
- data.php: data transaksi
- index.php: halaman struk
- assets/style.css: desain halaman
- pengujian.md: catatan pengujian
- bukti/: screenshot dan PDF

## Aturan Perhitungan
- Diskon 10% untuk subtotal minimal Rp50.000.
- Pajak simulasi 5% setelah diskon.
- Diskon dan pajak dibulatkan ke rupiah terdekat.
- Pajak hanya untuk simulasi pembelajaran.

## Hasil Data Awal
- Subtotal: Rp59.000
- Diskon: Rp5.900
- Setelah diskon: Rp53.100
- Pajak: Rp2.655
- Total: Rp55.755
- Bayar: Rp100.000
- Kembalian: Rp44.245

## Batasan
- Data diubah melalui data.php.
- Nomor dan waktu transaksi merupakan contoh tetap.
- Belum menggunakan form, session, dan database.
- Data harga dan jumlah mengikuti spesifikasi latihan.