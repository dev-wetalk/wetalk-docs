# Inbound Webhooks

Webhook masuk adalah alat yang ampuh untuk menerima data dari mana saja ke chatbot melalui permintaan POST.

Dengan webhook masuk, bot Anda bahkan dapat memulai percakapan dengan pengguna bot yang belum pernah berbicara dengannya sebelumnya.

Misalnya, saat klien mengisi informasi kontaknya di situs web Anda, Anda mengirimkan data tersebut ke webhook masuk dari chatbot, katakanlah bot SMS. Bot SMS kemudian dapat mengirim pesan konfirmasi ke nomor telepon klien.

Jika webhook itu dibuat dalam bot Suara, bot tersebut bahkan dapat langsung menghubungi klien!

## Buat Webhook Masuk
Ini tersedia di hampir semua saluran, di pembuat alur Anda, buka Alat - Webhook Masuk:

[gambar]

Klik New Inbound Webhook, beri nama dan klik Save:

[gambar]

Anda akan melihat antarmuka pengeditan seperti ini:

[gambar]

### Alamat webhook
Area ini menunjukkan kepada Anda ke mana harus mengirim data dan metodenya, yaitu POST. Setiap webhook masuk memiliki URL unik di seluruh sistem UChat.

### Contoh JSON yang Diterima
Area ini menunjukkan contoh JSON untuk referensi. Ini menggambarkan struktur data di JSON yang kami terima nanti. Kami membutuhkannya untuk menemukan nilai **identifikasi pengguna** dan data yang akan disimpan.

Ada 2 cara untuk mendapatkan contoh JSON:

1. ketik/tempel secara manual di sini
2. mendengarkan data real-time dari tes langsung

### Nilai untuk Mengidentifikasi Pengguna
Setiap kali webhook menerima data, pertama-tama webhook akan memeriksa jalur yang Anda tentukan di sini untuk melihat apakah dapat menemukan pengguna yang ada di chatbot.

Jika pengguna tidak ada dalam sistem, chatbot akan membuat profil baru. Begitulah cara chatbot memulai percakapan tanpa berbicara dengan pengguna sebelumnya.

Namun, beberapa saluran tidak mengizinkan chatbot untuk memulai percakapan terlebih dahulu karena masalah privasi dan spam.

Misalnya, bot SMS Anda dapat mengirim pesan selama Anda memiliki nomor telepon penerima, sedangkan chatbot Facebook Messenger Anda tidak dapat mengirim pesan ke pengguna Facebook yang belum pernah berbicara dengan bot Anda sebelumnya.

#### Proses Identifikasi Pengguna
Ini adalah proses bagaimana sistem mengidentifikasi pengguna:

1. periksa user_ns
  - jika ada user_ns yang valid, pengguna ditemukan.
  - jika tidak, langkah selanjutnya
2. cek telepon/email
  - jika kami dapat menemukan pengguna melalui telepon atau email, pengguna ditemukan.
  - jika tidak, langkah selanjutnya
3. verifikasi telepon
  - tidak ada pengguna yang cocok dalam sistem, apakah nomor teleponnya valid?
  - jika ya, profil pengguna dibuat.
  - jika tidak, webhook tidak akan diproses

### Pemetaan Wilayah
Daftar pemetaan menunjukkan nilai mana yang harus disimpan di bidang khusus mana. Saat Anda mendapatkan contoh JSON di area di atas, klik Preview Payload untuk mendapatkan alat pemetaan.

## Webhook Log

[gambar]

Setiap permintaan disimpan di Log. Klik catatan untuk melihat data JSON yang diterima.

## Demo: Konfirmasi Pemesanan
Alat yang sempurna untuk menguji webhook masuk Anda sudah terpasang di mana saja! Dapatkan chatbot sederhana (saluran apa pun), uji di Langkah Tindakan.

Buka halaman web UChat lain berdampingan, pertahankan pengeditan webhook masuk di Halaman 1 dan pilih permintaan eksternal di Halaman 2:

[gambar]

Ikuti langkah 1 hingga 8 di tangkapan layar berikut:

[gambar]

Berikan data yang perlu dikirim ke chatbot dan klik Uji, Anda pasti mendapatkan kesalahan "webhook tidak aktif" karena kami belum mengaktifkannya. Tidak apa-apa, klik Selesai di Halaman 1, dan Anda akan melihat data disimpan:
[gambar]

Gulir ke bawah sedikit, ikuti langkah 1, 2, 3 untuk memberi tahu sistem, di mana nilai telepon dan email di JSON:

[gambar]

Terakhir, petakan data lainnya ke chatbot:

[gambar]

Simpan pengeditan webhook masuk Anda:

[gambar]

Masukkan subflow, mari kirim pesan ke pengguna bot:

[gambar]

Publikasikan alurnya dan mari lakukan pengujian langsung di permintaan eksternal lagi:

[gambar]

Kami dapat melihat bahwa kali ini berjalan tanpa kesalahan karena kami mengaktifkan webhook dan menggunakan nomor telepon asli. Buka Log dan kita dapat melihat profil pengguna baru berhasil dibuat.

Di sisi pengguna:

[gambar]


