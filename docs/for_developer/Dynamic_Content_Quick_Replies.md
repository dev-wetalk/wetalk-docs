# Quick Replies

properti quick_replies dari respons server bersifat opsional. Balasan cepat tidak dapat digunakan dalam blok dinamis dari node konten jika ada blok lain setelahnya. Format deskripsi balasan cepat sama untuk tombol, mendukung jenis konten, node, dynamic_block_callback.

## Go to Node Quick Reply

[gambar]

kunci target harus ditautkan ke simpul yang ada dalam aliran yang dieksekusi. Nama node dapat ditemukan di headernya, Anda perlu menggunakan nama unik untuk node yang terhubung dengan tautan. Jika ada beberapa node dengan nama yang mirip di dalam aliran yang sama, perilaku transisi tidak akan memenuhi harapan. Balasan cepat buka simpul tidak didukung di API Publik.

## Dynamic Block Callback Quick Reply

Properti "header", "payload" bersifat opsional.

[gambar]