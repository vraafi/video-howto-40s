## Masalah
Tim butuh video tutorial 40 detik untuk produk how-to. Video harus punya 8 langkah bernomor, judul, penutup, dan resolusi 1280x720. Aset media dan kode harus siap dipakai tanpa langkah manual tambahan.

## Yang Dibangun
Kami membangun skrip `buat_video.py` berukuran 1607 B. Skrip ini menyusun video tutorial 40 detik: 8 langkah bernomor, judul, penutup, resolusi 1280x720. Keluaran utama berupa berkas skrip yang bisa dijalankan ulang. Fokus kami: satu berkas kecil, satu alur produksi, satu hasil yang bisa diperiksa.

## Keputusan Teknis
Kami memisahkan lapis kode dan lapis media. Dua lapis itu diperiksa terpisah. Keputusan ini membuat QC cepat dan batas masalah jelas. Kami memakai Python sebagai mesin penyusun video. Kami mencatat 1 berkas Python dan 11 berkas lain di luar daftar bahasa inti. Kami tidak menambah dependensi yang tidak perlu.

## Bukti (angka QC)
QC menyelesaikan 1,7 detik. Lapis aktif: kode dan media. Lapis lulus: kode dan media. Temuan: 0. Rincian kode: 1 Python, 0 JavaScript, 0 JSON, 0 Lua, 11 lain. Berkas hasil: `buat_video.py` (1607 B).

## Batasan
Uji QC mencakup dua lapis, kode dan media. Uji ini belum mengukur kualitas narasi atau keterbacaan teks di layar kecil. Video 1280x720 sudah sesuai spesifikasi, tetapi belum diuji di perangkat seluler low-end. Skrip belum menangani input media di luar format yang dipakai saat QC.