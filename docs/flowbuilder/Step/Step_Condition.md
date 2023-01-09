# Langkah Kondisi

Dengan langkah Kondisi, Anda dapat pergi ke langkah/sub alur yang berbeda tergantung pada kondisi.

[gambar]

Pada langkah Kondisi Anda, klik "+ Tambahkan Grup Kondisi" untuk menetapkan setidaknya satu grup kondisi. Grup "jika tidak" selalu ada.

Anda dapat membuat grup kondisi sebanyak yang Anda butuhkan. Pencocokan dimulai dari atas ke bawah, setelah grup cocok, sistem akan menuju ke langkah bernama. Jika gagal mencocokkan semua grup kondisi, grup "Otherwise" akan mengambil alihnya. Jadi selalu merupakan praktik yang baik untuk menyebutkan langkah dalam grup "Sebaliknya" meskipun sangat tidak mungkin untuk digunakan.

[gambar]

Hal lain yang penting untuk diketahui adalah perbedaan antara "Semua kondisi" dan "Kondisi apa saja". Itu duduk di sudut kanan atas setiap kelompok kondisi.

Anda dapat mencantumkan lebih dari 1 ketentuan dalam grup ketentuan. Ketika Anda melakukannya, penting apakah Anda memilih "Semua" atau "Apapun".

"Semua Kondisi" berarti untuk mencocokkan grup ini, Anda harus memiliki semua kondisi yang cocok di grup.

[gambar]

Namun, untuk mendapatkan grup dengan "Kondisi Apa Pun" yang cocok, Anda hanya perlu mencocokkan salah satu kondisi.

[gambar]

## Kondisi Tag & Urutan

[gambar]

Untuk kondisi tag dan urutan, Anda dapat memilih "masuk" atau "tidak masuk" dari "Operator". Memilih beberapa tag/urutan diperbolehkan.

## Kondisi Variabel Teks

[gambar]

Ini semua adalah operator untuk kondisi teks.

Untuk "memiliki nilai apa pun" dan "kosong" dari semua jenis variabel, saat Anda menghapus variabel, variabel tersebut menjadi kosong. Jadi, "memiliki nilai apa pun" salah dan "kosong" benar untuk variabel ini.

## Kondisi Variabel Angka

[gambar]

Ini semua adalah operator untuk kondisi angka.

## Kondisi Variabel DataTime

[gambar]

Ini semua adalah operator untuk kondisi DateTime.

Perhatikan bahwa Anda harus menempatkan "nilai" selalu sebagai format yang benar "yyyy-MM-dd HH:mm:ss" apa pun format tampilan yang Anda pilih untuk variabel itu.

## Kondisi Variabel JSON

[gambar]

Ini semua adalah operator untuk kondisi JSON.

## Masukan Kustom
Input khusus dibuat untuk membandingkan nilai dalam variabel JSON. Cari "input khusus" di bidang if:

[gambar]

Pilih nilai dari JSON, lalu Anda dapat membandingkannya saat menggunakan kondisi variabel teks.

## Rumus Matematika

[gambar]

Dengan operasi ini, Anda sekarang dapat melakukan penghitungan rumus secara langsung di Langkah Tindakan - "Tetapkan Nilai Variabel" dan Langkah Ketentuan - "Nilai".

Operasi matematika dan fungsi yang didukung:

+, -, *, e, pi, PI, abs(), min(), maks(), ceil(), lantai(), log(), pow(), bulat(), sqrt(), sin( ), cos(), tan()


