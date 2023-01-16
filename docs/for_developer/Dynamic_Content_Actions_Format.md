# Actions Format

properti tindakan dari respons server adalah opsional.

[gambar]

## Action Add Tag

Gunakan respons ini untuk menambahkan tag ke pelanggan. Tag dengan nama yang sama harus ada di bot Anda:

[gambar]

Nama tag yang dikirim menggunakan parameter tag_name harus cocok dengan salah satu tag yang ada dalam bot UChat

## Action Remove Tag

Gunakan respons ini untuk menghapus tag dari pelanggan. Tag dengan nama yang sama harus ada di bot Anda:

[gambar]

## Action set subscriber’s field value

Gunakan respons ini untuk menyetel nilai bidang pelanggan. Bidang khusus dengan nama yang sama harus ada di bot Anda

[gambar]

Filed name yang dikirim menggunakan field_name harus cocok dengan nama salah satu custom field yang ada di dalam bot UChat Anda perlu mengontrol tipe data yang tercatat di custom field, tipe data harus cocok dengan tipe custom field

Gunakan format nilai berikut:

Untuk bidang angka, nilai jenis harus numerik seperti 2 atau 3,14 tidak dibatasi oleh tanda kutip ganda;
Untuk nilai jenis bidang Teks harus ditransfer sebagai teks "beberapa teks";
Untuk nilai jenis bidang Tanggal harus ditransfer sebagai teks dengan format tanggal seperti YYYY-MM-DD, yaitu "25-03-2018";
Untuk nilai jenis bidang Tanggal Waktu harus ditransfer sebagai teks dengan tanggal yang diformat dalam ISO8601 UTC, yaitu "2018-03-25T13:25:00.000Z"

## Action unset subscriber’s field 

Gunakan respons ini untuk menghapus (menghapus) nilai bidang pelanggan. Bidang khusus dengan nama yang sama harus ada di bot Anda

[gambar]