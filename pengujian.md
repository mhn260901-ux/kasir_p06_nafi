# Pengujian Mini Project Struk Kasir

## Identitas
Nama:MUHAMMAD HANAFI NASUTION
NIM:25110057
Kelas:TK D SIANG
Versi PHP:8.2

## Hasil Pengujian

| No | Skenario | Hasil harapan | Hasil aktual | Status |
|---|---|---|---|---|
| 1 | Data awal | Total Rp55.755 dan kembali Rp44.245 | | LULUS |
| 2 | Bayar pas | Kembalian Rp0 dan status LUNAS | | LULUS |
| 3 | Bayar Rp50.000 | Kekurangan Rp5.755 | | LULUS |
| 4 | Subtotal Rp49.999 | Diskon Rp0 dan total Rp52.499 | | LULUS |
| 5 | Subtotal Rp50.000 | Diskon Rp5.000 dan total Rp47.250 | | LULUS |
| 6 | Nama produk | Pulpen Biru | | LULUS |
| 7 | Waktu transaksi | 21/10/2026 15:30 WIB | | LULUS |
| 8 | Pemulihan data awal | Tiga produk kembali tampil | | LULUS |

## Masalah dan Perbaikan
Tuliskan masalah yang dialami dan cara memperbaikinya.

## Jawaban Pemahaman
1. Mengapa harga disimpan sebagai angka?
2. Apa kegunaan fungsi hitungSubtotal()?
3. Kapan diskon diberikan?
4. Mengapa pajak dihitung setelah diskon?
5. Apa perbedaan trim() dengan e()?
6. Mengapa pembayaran kurang tidak ditampilkan sebagai kembalian negatif?
7. Apa fungsi foreach pada index.php?

## Sumber dan Bantuan
Tuliskan sumber atau bantuan yang digunakan.
1. Harga disimpan sebagai angka (seperti integer atau float/decimal) agar sistem dapat melakukan operasi matematika seperti penjumlahan, perkalian diskon, dan perhitungan pajak. Jika disimpan sebagai teks (string), sistem tidak bisa menghitungnya secara langsung.
2. Fungsi hitungSubtotal() berguna untuk menghitung total harga awal dari seluruh barang yang dibeli sebelum dikurangi diskon atau ditambah pajak. Biasanya dilakukan dengan mengalikan harga barang × jumlah (quantity).
3. Diskon diberikan sebelum pajak dihitung. Secara logika bisnis, diskon diterapkan ketika transaksi memenuhi syarat tertentu, seperti mencapai minimum pembelian, menggunakan kode promo, atau adanya event potongan harga khusus.
4. Pajak dihitung setelah diskon karena pajak (seperti PPN) hanya dikenakan pada nilai riil yang dibayarkan oleh pembeli. Jika pajak dihitung sebelum diskon, pembeli akan membayar pajak yang lebih besar dari yang seharusnya, yang secara regulasi hukum keuangan umumnya tidak sah.
5. Kedua fungsi ini memiliki tujuan keamanan dan kerapian data yang berbeda:
• trim(): Berfungsi untuk menghapus spasi kosong di awal dan di akhir sebuah teks (string).
• e() (atau htmlspecialchars() di PHP): Berfungsi untuk mengubah karakter HTML khusus menjadi teks aman (escaping) untuk mencegah serangan siber seperti Cross-Site Scripting (XSS).
6. Pembayaran kurang tidak ditampilkan sebagai kembalian negatif demi kejelasan visual dan pengalaman pengguna (UX). Dalam sistem kasir atau e-commerce, uang kembalian secara definisi adalah uang yang dikembalikan kepada pelanggan. Jika kurang, sistem biasanya akan menampilkan pesan eror atau keterangan "Kekurangan Pembayaran" agar kasir atau pembeli tidak bingung.
7. Fungsi foreach pada index.php adalah untuk mengulang (looping) dan menampilkan data array satu per satu ke layar halaman web. Biasanya digunakan untuk menampilkan daftar produk di katalog atau daftar item belanjaan di dalam keranjang secara otomatis.