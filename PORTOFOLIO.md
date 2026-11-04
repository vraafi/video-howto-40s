## Masalah

Tim butuh video how-to 40 detik yang bisa diproduksi ulang tanpa editor. Tutorial manual memakan waktu dan tidak konsisten antar rilis.

## Yang Dibangun

Satu skrip `buat_video.py` yang menghasilkan video 1280x720: judul, 8 langkah bernomor, dan penutup dalam 40 detik. Skrip dan dokumentasi disertakan dalam dua berkas: `buat_video.py` (1743 B) dan `README.md` (819 B).

## Keputusan Teknis

- Satu berkas Python sebagai sumber kebenaran. Tidak ada dependensi tersembunyi di lapis kode.
- Struktur waktu tetap: 8 langkah bernomor memaksa durasi tiap langkah terukur.
- Resolusi dikunci di 1280x720 agar keluaran seragam.
- Lapis media dipisah dari lapis kode untuk QC.

## Bukti

QC selesai dalam 0,69 detik. Temuan: 0. Dua lapis aktif: kode dan media. Keduanya lulus. Sebaran berkas: 1 Python, 1 JSON, 15 lain, 0 JavaScript, 0 Lua.

## Batasan

Video ini bukan untuk produksi berskala besar. Tidak ada pengguna, klien, atau metrik adopsi yang diklaim. Isi langkah ditentukan manual; skrip hanya merangkai. Uji coba hanya menyentuh dua lapis QC, bukan seluruh pipeline distribusi.