# Action Step Send Notification

Tindakan ini memungkinkan bot Anda mengirimkan notifikasi melalui berbagai saluran, termasuk

- Surel
- Kendur
- SMS
- Panggilan telepon

[gambar]

Semuanya ada di "Pemberitahuan" langkah Tindakan Anda.

## Pemberitahuan email
Untuk mengirim notifikasi email, Anda harus menyiapkan integrasi email terlebih dahulu. Periksa cara menyiapkan integrasi email?

[gambar]

Tidak seperti langkah "Kirim Email", notifikasi email hanya mendukung jenis pesan teks. Centang langkah "Kirim Email" di halaman "Integrasi Email" jika Anda membutuhkan lebih banyak jenis pesan seperti gambar, tombol, file, dll.

Cantumkan alamat pengirim di "Email Profile" dan alamat penerima di "To Email".

## Slack Notifikasi
Demikian pula, untuk mengirim notifikasi slack, Anda harus menyiapkan integrasi slack terlebih dahulu. Periksa cara menyiapkan slack integration?

[gambar]

Di jendela pop-up,

1. pilih Webhook
2. pilih saluran default atau beri nama yang lain
3. pilih jenis pesan, tambahkan sebanyak yang diperlukan
4. misalnya, ketik "Bagian", letakkan pesan Anda di area 4 dan tambahkan nilai foto atau bidang jika perlu
5. gunakan tombol "Uji" untuk mengirim pesan untuk pengujian dan sesuaikan
6. setelah selesai, klik "Simpan".

## SMS Pemberitahuan
Siapkan nomor pengirim sebelum Anda membuat notifikasi SMS. Periksa bagaimana cara menambahkan nomor telepon?

[gambar]

Anda dapat menggunakan operasi "hasilkan teks acak" dengan variabel teks untuk mendapatkan kode keamanan acak dan mengirimkannya untuk tujuan verifikasi yang ditunjukkan pada gambar.

[gambar]

Pilih pengirim dan penerima, masukkan pesan dan ini dia!

## Lakukan Panggilan Telepon
Sama seperti notifikasi SMS, nomor telepon diperlukan untuk melakukan panggilan telepon. Periksa bagaimana cara menambahkan nomor telepon?

Selain itu, Anda harus membuat aliran suara terhubung ke nomor telepon ini jika tidak bot suara Anda tidak tahu harus berkata apa.

[gambar]

### Muatan Ref
Ref payload digunakan untuk meneruskan pesan ke bot suara.

Misalnya, setel payload ke "dukungan" di sini di tindakan notifikasi dan di aliran suara Anda:

[gambar]

Pergi ke Langkah Awal di Alur Utama Anda dan simpan payload referensi di bidang khusus.
