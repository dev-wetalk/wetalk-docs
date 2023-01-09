# Langkah Kirim Pesan
Setelah membuat aliran pertama Anda, buka, klik "Edit Aliran", buat bot Anda berdampingan dan ini dia! 😆
Mari kita ambil Facebook sebagai contoh. Alur lain berbagi proses serupa di mana perbedaan utamanya adalah jenis pesan.

[gambar]

Beberapa langkah sederhana untuk mengirimkan pesan pertama Anda:

1. klik titik awal berwarna hijau
2. di panel edit, "Pilih Langkah Berikutnya"
3. pilih langkah "Kirim Pesan".
4. klik langkah "Kirim Pesan".
5. klik pesan jenis teks
6. Masukkan pesan Anda
7. "Menerbitkan"

[gambar]

Itu dia! Mari kita uji!

[gambar]

Klik "Pratinjau" dari bilah navigasi dan "Buka alur di Messenger". Klik "Mulai" jika ini pertama kalinya Anda berbicara dengan bot.

[gambar]

Selamat! Bot Anda bekerja sekarang. 🤖🤖

Biarkan saya menunjukkan kepada Anda beberapa detail lebih lanjut tentang langkah Kirim Pesan. Ini adalah jenis pesan yang sama untuk semua/beberapa Saluran. Periksa berdasarkan jenis di bawah ini:

## Kirim Teks / Variabel

[gambar]

UChat telah terintegrasi dengan Grammarly untuk membantu Anda mendapatkan ekspresi yang sempurna.

[gambar]

## Masukkan Nilai Bidang Khusus dan Emoji
Di mana pun Anda melihat "</>", Anda dapat memasukkan emoji atau nilai variabel ke teks.

[gambar]

Atau cukup ketik "{{" untuk memanggil daftar bidang:

[gambar]

## Kirim Gambar / Audio / Video / File
Totalnya ada 4 cara:

[gambar]

- unggah dari komputer Anda (ukuran terbatas)
> |     Media Type     | Maximum Upload Size |
|:------------------:|:-------------------:|
|        video       |         10MB        |
|        audio       |         5MB         |
|        file        |         5MB         |
| others(e.g. image) |         2MB         |

- dari tautan URL (DISARANKAN)
> Anda dapat mencari gambar secara online dan menyalin tautan URL langsung mereka. Tetapi tautan langsung ini mungkin berubah. Alternatifnya, Anda dapat mengunggah foto ke server Anda atau penyimpanan foto pihak ketiga lainnya seperti imgur.com, lalu dapatkan tautan URL langsung dari situ. Tautan URL langsung berarti tautan tersebut mengarah ke foto tertentu, bukan situs web, diakhiri dengan .jpg atau .png, dll. Ambil tautan pada gambar di atas sebagai contoh.

- cari dari galeri GIF
> UChat memberi Anda galeri GIF, Anda dapat mencari apa yang Anda butuhkan di sini.

- dari Perpustakaan
> Perpustakaan adalah tempat Anda dapat melihat semua foto, GIF, audio, dan video yang telah Anda unggah sebelumnya. Agar tidak perlu mengupload ulang media yang sama, cari saja di perpustakaan Anda.

## Send Card

[gambar]

Kartu digunakan untuk menampilkan berbagai informasi secara apik seperti informasi produk. Ada 4 faktor dalam kartu, gambar, judul, subtitle dan tombol.

## Kirim "Untuk Setiap"
Jenis pesan ini juga menampilkan kartu tetapi dengan cara yang lebih otomatis. Dengan "Untuk Setiap", Anda tidak perlu mengetik sendiri setiap kartu. Secara otomatis menampilkan semua item dalam variabel JSON. Periksa Langkah Tindakan - Operasi JSON jika Anda tidak tahu apa itu variabel JSON.

[gambar]

pilih variabel JSON terlebih dahulu
klik "</>" atau ketik "{{" di kotak teks
pilih "ITEM" untuk mendapatkan sampel item dari variabel JSON
Nilai dalam variabel JSON:

[gambar]

Nilai dalam "ITEM":

[gambar]

"Data sampel" adalah mengisi kolom "Jalur JSON" dengan cepat. Misalnya, seperti yang ditunjukkan pada gambar, klik baris "price", dan "$.price" muncul di "JSON Path" itu sendiri. Artinya, kami menampilkan harga setiap item di sini. Jika tidak ada data sampel yang diminta, Anda dapat mengisi jalur sendiri dengan mengetikkan "$.", yang merujuk ke setiap item dalam variabel JSON, diikuti dengan kunci nilai.

### Format Nilai
Selain itu, untuk angka seperti persentase dan harga, untuk nilai tanggal dan nilai waktu, UChat memiliki format berbeda untuk Anda. Misalnya, pada gambar di atas, nilai harganya adalah "5" dan setelah memilih format "F03", bot akan menampilkannya sebagai "$5". Sedangkan nilai pada variabel masih berupa angka "5" sehingga dapat digunakan dalam perhitungan matematika atau perbandingan kondisi tanpa malfungsi.

### Kunci Tersembunyi
Besar! Sekarang Anda lihat bagaimana menggunakan "Untuk Setiap". Selain kunci dalam variabel JSON, ada 3 kunci tersembunyi yang mungkin Anda perlukan:

[gambar]

| Key Name |             Description             |
|:--------:|:-----------------------------------:|
|   INDEX  |   index of the item started from 1  |
|    KEY   |         key name of the item        |
|   VALUE  | value of the item = the item itself |

### Contoh INDEKS
Saat Anda memiliki JSON dengan daftar JSON di dalamnya, gunakan INDEX untuk memeriksa nomor urut suatu item. Mari tambahkan nomor indeks sebelum nama item:

[gambar]

Hasil pengujian:

[gambar]

### Contoh KUNCI/NILAI
Saat Anda memiliki JSON seperti yang ditunjukkan pada gambar berikut alih-alih JSON yang menyimpan daftar JSON,

[gambar]

Inilah yang akan Anda dapatkan dengan menggunakan tiga kunci:

[gambar]

Hasil pengujian:

[gambar]

## Kirim SELECT setelah "Untuk Setiap"
Saat Anda menambahkan tombol ke "Untuk Setiap", tombol tersebut akan ditampilkan dengan setiap kartu. Biasanya, Anda mungkin ingin meletakkan tombol "Beli" atau "Pilih" di sini jika Anda mencantumkan beberapa produk atau opsi.

Bagaimana bot mengetahui kartu mana yang dipilih pengguna?

[gambar]

Saat Anda memilih langkah selanjutnya untuk tombol, pilih "Pilih":

[gambar]


Kemudian pilih langkah berikutnya seperti yang biasa Anda lakukan, seperti Langkah Kirim Pesan untuk menampilkan item yang dipilih atau Langkah Tindakan untuk menangani data. Anda kemudian dapat mengakses item yang dipilih di "PILIH":

[gambar]

Misalnya, mari tambahkan langkah Kirim Pesan, temukan bidang sistem "PILIH":

[gambar]

1. klik baris "item" untuk mendapatkan jalur "$.item" atau ketik jalur secara langsung
2. di jalur JSON, tambahkan nama kunci jika perlu. Dalam hal ini, mari tunjukkan nama item yang dipilih. Jadi tambahkan ".name" setelah path.

[gambar]

Anda akan melihat ini saat mengujinya:

[gambar]

## Kirim Konten Dinamis
Konten Dinamis membantu Anda mengirimkan permintaan API, ke server Anda atau server pihak ketiga, untuk mendapatkan respons untuk ditampilkan. Server dapat membalas secara berbeda setiap kali. Dengan cara ini, bot Anda dapat menampilkan konten dinamis kepada pengguna Anda.

Fitur ini praktis ketika logika bot Anda rumit dan sangat bergantung pada server lain. Misalnya, Anda memiliki algoritme AI sendiri untuk menganalisis pertanyaan pengguna dan menghitung respons yang sesuai di server Anda, dalam hal ini, Anda dapat mengirimkan pertanyaan dalam permintaan API. Dan server dapat menghasilkan respons berdasarkan pertanyaan tersebut. Terakhir, server mengirimkan respons kembali ke UChat untuk ditampilkan kepada pengguna Anda.

Pesan respons dapat berisi beberapa pesan, tombol, dan balasan cepat dengan tindakan. Anda bahkan dapat menerapkan tindakan sederhana seperti menambahkan tag secara langsung di respons JSON.

- Periksa Langkah Tindakan - Permintaan Eksternal untuk cara mengirim permintaan API,
- dan Format Respons untuk panduan pemformatan pesan.

## Mengirim Lokasi

[gambar]

Untuk mengirim lokasi, cari di peta, lalu klik kanan untuk menyalin nilai lintang dan bujurnya:

[gambar]

Masukkan nama lokasi Anda, rekatkan data dan tambahkan label jika perlu. Label memberikan informasi tambahan seperti lantai atau nomor kamar.

[gambar]

## Kirim Produk Ecommerce
Periksa E-niaga untuk cara menyiapkan dan menggunakan sistem e-niaga bawaan.

## Facebook - Kirim Pesan
Facebook memungkinkan bot untuk mengirim teks dengan 3 tombol dan 10 balasan cepat paling banyak.

### Kirim Teks dengan Tombol & Balas Cepat

[gambar]

Perbedaan antara tombol dan balasan cepat di Facebook Messenger:

|     Type    | Usage                                               |
|:-----------:|-----------------------------------------------------|
|    button   | once sent, always in the conversation to be pressed |
| quick reply | similar to button, but disappear when used          |

Try to add some buttons, quick replies and test it. You will see their differences.

## Telegram - Kirim Pesan
Aliran Telegram adalah jenis aliran kami yang baru ditambahkan. Ini mirip dengan aliran Facebook kecuali untuk beberapa fitur eksklusif dengan Facebook. Silakan periksa alur Facebook untuk panduan untuk saat ini. Tutorial teks tentang aliran Telegram akan segera diperbarui.

## WeChat - Kirim Pesan
WeChat memungkinkan bot mengirim teks paling banyak dengan 10 tombol. Jenis pesan dengan WeChat:

[gambar]

### Mengirim Artikel

[gambar]

Ini penampakan di chatnya :

[gambar]

### Kirim Program Mini
Anda juga dapat mengirim program mini yang terkait dengan akun resmi Anda.
[gambar]

## WhatsApp - Kirim Pesan
Jenis pesan dengan WhatsApp:

[gambar]

Tombol di WhatsApp sedikit berbeda dengan yang ada di Facebook. Tombol di Facebook bisa ditekan berkali-kali sedangkan di WhatsApp, hanya sekali.

## SMS - Kirim Pesan
Bot SMS hanya dapat mengirim teks dan gambar.

[gambar]
## Suara - Kirim Pesan
### Kirim Teks / Audio

[gambar]

Anda dapat membuat bot membacakan teks dengan bahasa tertentu atau merekam audio Anda sendiri dan mengunggahnya.

UChat telah membangun Aplikasi Mini yang disebut "VoiceMaker" menggunakan API pihak ketiga yang memberi Anda kualitas konversi teks-ke-suara yang lebih baik! Unduh Aplikasi Mini di bagian integrasi. Dokumentasi tentang "VoiceMaker" sedang dalam proses.

## Google Bisnisku - Kirim Pesan
Jenis pesan dengan alur Google bisnisku:

[gambar]

Semua jenis tercakup di atas, harap periksa jenis pesan yang sama untuk semua/sebagian saluran. Temukan jenis lokasi di "Media Kaya".
