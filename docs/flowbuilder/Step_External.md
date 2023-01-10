# Action Step External Request

Dengan permintaan eksternal, Anda dapat memanggil API dari pihak ketiga lain atau server Anda sendiri untuk meminta data, mengirimkan data, dll.

[gambar]

Pada langkah Tindakan, temukan "Permintaan Eksternal" di "Tindakan Lanjutan" dan klik "Tambahkan permintaan Anda", lalu mulailah mengeditnya:

[gambar]

1. pilih jenis permintaan seperti GET, POST, dll
2. rekatkan URL / titik akhir permintaan Anda
3. sesuaikan bagian "parameter URL", "Headers", "Body" atau "Otorisasi" jika diperlukan. misalnya kunci API penyiapan
4. klik "Uji" dan area 5 akan ditampilkan di bagian "Respon" dengan kode respons
5. klik "Respon Header" untuk memperluas header untuk detail lebih lanjut dan data yang diterima berwarna biru
6. pilih bagian mana dari data yang Anda butuhkan dengan mengklik lingkaran di sisi kiri yang sesuai
7. setelah mengklik area 6, jalur JSON untuk data yang dipilih secara otomatis ditampilkan di sini. $ berarti seluruh JSON.
8. pilih bidang khusus mana untuk menyimpan data. Anda dapat membuat bidang baru di sini dengan mengetikkan nama bidang dan mengekliknya di drop-down. Klik tombol "Tambah" untuk menambahkan ke daftar pemetaan
9. terakhir, pemetaan ditampilkan di area 9. Tambahkan pemetaan sebanyak yang diperlukan dan klik "Simpan".

## Parameter URL

[gambar]

Pada tangkapan layar di atas, kita dapat melihat bahwa ada parameter URL di titik akhir yang disebut "nama_pengguna". Ingatlah untuk menyalin titik akhir ke bawah dan memberikan nilai pengujian.

Atau, Anda dapat menggunakan bagian Params URL untuk hasil yang sama.

## Header

[gambar]

Sama seperti Params URL, masukkan nama kunci Anda terlebih dahulu, lalu masukkan variabel dan berikan nilai pengujian.

## Otorisasi

[gambar]

Alternatifnya, letakkan token di bagian Otorisasi. Ini akan mengurangi rawan kesalahan (terkadang orang lupa "Beruang" di depan token).

Selain itu, untuk Basic Auth, cukup masukkan nilai nama pengguna dan kata sandi Anda dan sistem akan melakukan pengkodean base64 untuk Anda.

## Tubuh
Untuk memasukkan file itu sendiri ke dalam parameter, gunakan multipart/form-data:

[gambar]

x-www-for-urlencoded berfungsi seperti bagian Params atau Header URL.

Alih-alih mencantumkan semua payload di x-www-form-urlencoded, Anda juga dapat menempelkan contoh payload di JSON mentah:

[gambar]

Di sisi kiri, Isi Isi, rekatkan atau tulis JSON Anda terlebih dahulu, saat Anda memasukkan variabel, isi isi Tes langsung muncul di sisi kanan. Ini untuk menentukan nilai pengujian JSON.

Klik Salin dari konten tubuh untuk menyalin seluruh struktur JSON. Semua variabel akan diganti dengan {{variable_name}}. Hapus placeholder dan masukkan nilai pengujian Anda.

## Pengujian
Setelah Anda siap, klik tombol Uji di sebelah titik akhir URL atau di bagian Tanggapan.

[gambar]

Selain tips tentang cara memetakan data di atas, Anda mungkin juga ingin menyimpan nilai di header respons untuk digunakan nanti. Cukup luaskan tajuk, klik pada nilai di tajuk dan jalur JSON untuk ditampilkan secara otomatis di sana.


