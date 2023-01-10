# Question Step

[gambar]

## Tetapkan Jawaban Cepat
Jawaban cepat nyaman bagi pengguna untuk mengklik daripada mengetik. Saat Anda menyetel jawaban cepat:

[gambar]

"Teks Jawaban" ditampilkan kepada pengguna sementara "Nilai Jawaban" disimpan ke variabel.

### Bagaimana cara memberi prompt dan mengatur jawaban cepat?
Pada kotak pertanyaan misalnya isikan "reply 1 for service A, reply 2 for service B", dst. Kemudian pada quick answer, atur "Answer Text" menjadi "1", "2", dst untuk pencocokan, dan "Nilai Jawaban" menjadi "layanan A", "layanan B", dll untuk menyimpan opsi pengguna.

|  Channel |                            How to Provide Quick Answers                            |
|:--------:|:----------------------------------------------------------------------------------:|
| Facebook |                     quick answers will be displayed as buttons                     |
| Telegram |                     quick answers will be displayed as buttons                     |
|  WeChat  |                 use buttons instead of quick answer or give prompt                 |
| WhatsApp |                     quick answers will show in "Select Option"                     |
|    SMS   |                                     give prompt                                    |
|   Voice  | give prompt and use Speech question or DTMF question to ask for keypad/voice input |
|  Google  |                     quick answers will be displayed as buttons                     |

### Bagaimana cara kerja pencocokan dalam jawaban cepat?

[gambar]

Setelah input pengguna berisi salah satu "Teks Jawaban", jawaban cepat akan dicocokkan (tidak peka huruf besar/kecil). Plus, urutan jawaban cepat itu penting karena bot akan memeriksa secara berurutan. Setelah jawaban cepat cocok, itu akan menghentikan pencocokan.

[gambar]

## Tombol Lewati
Tambahkan tombol lewati jika pertanyaan boleh dilewati. Selain itu, label tombol lewati dapat diedit.

## Tidak Cocok

[gambar]

"No Match" adalah fitur yang sangat praktis karena tipe jawaban yang berbeda memiliki pola yang ditentukan berbeda. Alamat email, misalnya, harus "xxx@xx.xx". Anda dapat memasukkan sesuatu seperti "Email salah, silakan coba lagi" sebagai pesan coba lagi dan lompat ke langkah lain jika tidak ada yang cocok beberapa kali.

Namun, format "xxx@xx.xx" hanya menyaring email yang salah tetapi email palsu. Untuk memeriksa apakah email itu asli atau tidak, coba Aplikasi Mini untuk menggunakan alat verifikasi pihak ketiga.

## Tidak Ada Masukan
Demikian pula, "Tanpa Input" membantu Anda mengarahkan aliran saat input pengguna kedaluwarsa. Secara default, pertanyaan kedaluwarsa dalam 1 jam. Buat lebih pendek jika diperlukan.

[gambar]

## Minta Gambar / Audio / Video / File / Rekam

[gambar]

Saat pengguna mengunggah dokumen, tautan URL yang menunjuk ke dokumen disimpan dalam variabel, bukan di dokumen itu sendiri. Karena dokumen media bisa sangat besar. Nanti, jika Anda ingin mengirim dokumen itu di langkah kirim pesan, Anda harus memilih "Kirim Media Dari URL" dan ketikkan variabel di sana.

[gambar]

## Minta Pilihan
Ini adalah jenis pertanyaan yang mencantumkan jawaban cepat terbatas dan pengguna harus memilih hanya dari jawaban cepat ini. Misalnya, saat memilih jenis properti, cantumkan hanya rumah, townhouse, dan apartemen sebagai jawaban cepat. Oleh karena itu, jika pengguna tidak mengklik salah satu dari ketiganya, pesan coba lagi akan muncul.

## Tanyakan Tanggal / Waktu

## Minta Telepon
Validasi dasar untuk Pertanyaan nomor telepon adalah:
- hanya 11 karakter yang diperbolehkan: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, +.
- Tanda "+" hanya diperbolehkan di bagian depan ponsel
- lebih dari 6 karakter

## Langkah Pertanyaan di Bot Suara

[gambar]

[gambar]

## Bot Suara - Minta Ucapan
Pidato biasanya digunakan untuk mendapatkan jawaban singkat. Saat bot meminta input ucapan, bot akan mendengarkan apa yang dikatakan pengguna dan mengonversi ucapan menjadi teks dengan skor percaya diri. Skornya antara 0 dan 1. Semakin mendekati 1, semakin percaya diri analisis ucapannya.

Gunakan "Pengaturan Lanjutan" untuk membantu meningkatkan konversi:

[gambar]

Pilih model dan bahasa ucapan yang sesuai. Mode ucapan "Angka dan Perintah" dapat membantu meningkatkan tingkat pengenalan ketika jawabannya adalah serangkaian angka, dll. Harap dicatat bahwa, Twilio mengenakan biaya untuk menggunakan mode ini. Lebih penting lagi, berikan bot beberapa petunjuk, kata kunci yang mungkin muncul dalam ucapan (dipisahkan dengan koma dan tanpa spasi).

## Voice Bot - Minta DTMF (Keypad)
DTMF mengacu pada input keypad, termasuk angka 0 hingga 9, * dan #. Biasanya digunakan untuk membuat menu utama untuk bot suara Anda, seperti yang mungkin Anda dengar sebelumnya "Hai, tekan 1 untuk xxx, tekan 2 untuk xxx, ..."

[gambar]

"Jumlah Digit" berarti berapa banyak digit yang diharapkan. Misalnya, nomor kartu kredit membutuhkan 14 atau 16 digit sedangkan kode pos membutuhkan 4 atau 6 digit.

"Stop Key" diatur ke "#" secara default, tetapi juga dapat diedit. Anda akan membutuhkan "Stop Key" ketika Anda tidak tahu berapa banyak angka yang diharapkan. Jangan lupa menyebutkan "Tombol Berhenti" di kotak pertanyaan. 🤖🤖

## Bot Suara - Minta Rekaman

[gambar]

Sekali lagi, sama seperti meminta gambar, audio, video atau file, Anda memerlukan variabel teks untuk menyimpan tautan URL dari file rekaman. Periksa pengaturan lanjutan untuk detail lebih lanjut seperti "Stop Key" dan "Max Record Duration".

Anda akan dapat mengakses file rekaman melalui tautan URL atau secara manual dari bagian "Rekaman" yang ditunjukkan di bawah ini:

[gambar]

Di sini Anda dapat melihat semua rekaman "Rekam Pertanyaan" dan "Transfer" Anda dengan tombol "Putar" untuk memutar audio.

## Voice Bot - Minta Transfer
Fitur transfer lebih seperti Tindakan daripada Pertanyaan. Karena tindakan di langkah Tindakan dibagikan di semua saluran, kami menempatkan transfer di langkah Pertanyaan.

[gambar]

Anda dapat merekam percakapan setelah mentransfer untuk tujuan pelatihan, dll. Demikian pula, periksa rekaman dari bagian "Rekaman" dari sidebar kiri.

### Tutup Panggilan
Satu hal lagi, jika klien Anda perlu kembali ke bot setelah percakapan yang ditransfer. Ada 2 cara untuk melakukannya:

- pihak yang ditransfer menutup telepon terlebih dahulu
- klien Anda menekan tombol bintang (harus mengaktifkan opsi di setelan lanjutan)
Bagaimanapun, jangan lupa untuk menyebutkannya kepada klien Anda sebelum transfer.

### Tambahkan Ekstensi ke Nomor Telepon
Tambahkan ekstensi ke nomor telepon menggunakan kunci hash. misalnya +61412345678#wwww1234. Setiap "w" akan menunggu selama setengah detik.

Katakanlah saya memiliki bot suara untuk nomor +61412345678, dan saya mengajukan pertanyaan DTMF setelah titik awal aliran utama. Ekstensi "1234" akan dipertimbangkan sebagai masukan untuk pertanyaan DTMF ini. Dengan cara ini, Anda merutekan panggilan secara otomatis.

### Transfer ke Beberapa Nomor
Anda dapat memasukkan beberapa nomor di bidang "Transfer Ke Nomor Telepon", dipisahkan HANYA dengan koma. misalnya +61412345678,+61412345679#wwww1234,+61412345670

Bot akan memanggil 3 nomor ini secara bersamaan, orang pertama yang menjawab panggilan mendapatkan transfer ini, panggilan lainnya berhenti berdering. Penyedia nomor telepon Anda hanya akan menagih Anda untuk satu panggilan karena hanya satu nomor yang berhasil ditransfer.

## Bot Suara - Minta Pembayaran
Fitur pembayaran lebih seperti Tindakan daripada Pertanyaan.

[gambar]

[gambar]

### Mode PCI (Twilio)
Untuk pengguna Twilio, Anda harus mengaktifkan mode PCI di akun Twilio Anda untuk menerima pembayaran baik dalam mode percobaan atau langsung.

Cari "Pengaturan Suara" dari akun Anda,

[gambar]

klik tombol "Aktifkan":

[gambar]

### Sunting Perintah
Semua petunjuk sudah disetel dalam bahasa Inggris. Jangan ragu untuk mengubahnya jika diperlukan seperti mengubah ke bahasa lain. Ada 4 informasi yang harus dikumpulkan untuk sebuah kartu.

1. nomor kartu kredit
2. tanggal habis tempo
3. CVV
4. kode pos (jika perlu, aktifkan opsi di setelan lanjutan).

Setiap informasi memiliki 3 ucapan untuk disetel, ditanyakan, batas waktu, dan tidak valid:

[gambar]

### Konektor Pembayaran
Untuk mendapatkan "Konektor Pembayaran", yaitu "ID konektor unik", Anda harus mengakses penyedia nomor telepon dan penyedia layanan pembayaran Anda. Twilio dan Stripe, misalnya buka twilio.com (membuka jendela baru), ikuti langkah 1 hingga 4 pada 2 gambar berikut:

[gambar]

[gambar]

[gambar]

Instal, beri nama "NAMA UNIK" sendiri dan klik "Hubungkan dengan Stripe". "NAMA UNIK" ini kemudian menjadi "ID konektor unik" Anda, salin kembali ke UChat.

[gambar]

### Jumlah biaya
Masukkan angka langsung seperti "99,99" atau variabel angka di sini.

### Tanggapan

[gambar]

Anda memerlukan variabel JSON untuk menampung hasil pembayaran. Ini adalah contoh respon termasuk beberapa rincian kartu, kode konfirmasi dan hasil pembayaran.

### Pembayaran Gagal
Anda dapat menangani situasi tersebut melalui opsi "Pembayaran Gagal". Misalnya, kirim "Ada yang tidak beres" dan buka Langkah Pembayaran lagi.

### Token Satu Kali
Anda dapat memilih untuk mengambil pembayaran sekarang atau nanti.

- Jika Anda memutuskan untuk langsung menagih:
> beri nilai lebih dari 0 pada kotak "Charge Amount".

- Jika Anda ingin mendapatkan pembayaran nanti
> beri tanda "0" di kotak "Jumlah Biaya". Dengan cara ini, Anda akan mendapatkan token untuk penangkapan di masa mendatang.

Dalam situasi di mana Anda menetapkan jumlah tagihan ke "0", jika Anda mengaktifkan opsi "Token Satu Kali" di pengaturan lanjutan, Anda akan mendapatkan token satu kali. Kalau tidak, Anda mendapatkan token yang dapat digunakan kembali.

Dengan kombinasi jumlah tagihan yang berbeda dan opsi "Token Sekali Pakai", Anda akan mendapatkan hasil pembayaran yang berbeda:

| Charge Amount | One Time Token |  What Will Happen  | Payment Result |
|:-------------:|:--------------:|:------------------:|:--------------:|
|       0       |     Enabled    | get one-time token |     [gambar]   |
|  > 0, e.g. 5  |     Enabled    |      charge $5     |     [gambar]   |
|       0       |    Disabled    | get reusable token |     [gambar]   |
|  > 0, e.g. 5  |    Disabled    |      charge $5     |     [gambar]   |

Artinya, setiap kali Anda menetapkan jumlah tagihan lebih besar dari 0, tidak masalah apakah Anda mengaktifkan opsi Token Satu Kali atau tidak, Anda akan segera menagih klien Anda dan mendapatkan kode konfirmasi pembayaran. Kode dimulai dengan "ch_" jika Anda menggunakan Twilio.

Sebaliknya, token satu kali dimulai dengan "tok_" jika Anda menggunakan Twilio. Dan token yang dapat digunakan kembali mengacu pada ID pelanggan, dimulai dengan "cus_" jika Anda menggunakan Stripe.

### Cara Mengisi dengan Token
Periksa dokumentasi tentang cara membuat tagihan dengan penyedia layanan pembayaran Anda. Mari kita ambil Stipe sebagai contoh, untuk melakukan pembayaran dengan token yang dapat digunakan kembali.

[gambar]

Dalam contoh, permintaan pos dikirim ke Stripe dengan kunci API pengujian dan jumlah tagihan, mata uang, dan token yang dapat digunakan kembali, yaitu ID pelanggan.

[gambar]

Setelah menekan tombol test, berikut respon jika berhasil:

[gambar]

Dalam tanggapan Anda dapat melihat ada id yang dimulai dengan "ch_", yang merupakan kode konfirmasi pembayaran. Artinya, Anda telah berhasil melakukan pembayaran.

### Keterangan
"Deskripsi" dikirimkan bersama dengan detail pembayaran. Misalnya, Anda dapat memasukkan “Pembayaran sebesar $20,52 dikirimkan dari Nomor Telepon (xxx)-xxx-xxxx” untuk membuat rekaman guna menunjukkan panggilan mana yang melakukan pembayaran.

### Kartu Kredit untuk Pengujian
Gunakan detail kartu berikut untuk pengujian jika diperlukan:

> Credit card number: 4242 4242 4242 4242  
Expiry date (MM/YY): 12 25 (pick a date in the future)  
Zip code: 94105  
CVC security code: 333  
