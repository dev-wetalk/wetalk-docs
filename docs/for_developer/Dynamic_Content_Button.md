# Buttons

Anda dapat menggunakan tombol dengan setiap jenis: call, url, node.

[gambar]

## Call Button

[gambar]

## Url Button

Ada 3 opsi webview_size:

penuh - (100%),

sedang - (75%),

kompak - (50%)

Properti "webview_size" bersifat opsional.

[gambar]

## Go to Node Button

[gambar]

kunci target harus ditautkan ke simpul yang ada dalam aliran yang dieksekusi. Nama node dapat ditemukan di headernya, Anda perlu menggunakan nama unik untuk node yang terhubung dengan tautan. Jika ada beberapa node dengan nama yang mirip di dalam aliran yang sama, perilaku transisi tidak akan memenuhi harapan. Tombol buka simpul tidak didukung di API Publik

## Dynamic Block Callback Button

Properti "header", "payload" bersifat opsional.

[gambar]

dynamic_block_callback bekerja dengan cara yang sama seperti blok dinamis di node konten, itu akan mengirim permintaan ke server setelah klik, balasan server akan dikirim ke pengguna. URL server eksternal harus disebutkan dengan protokol HTTPS.
