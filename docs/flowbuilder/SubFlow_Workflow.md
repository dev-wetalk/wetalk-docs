# Workflow

Alur kerja dapat dianggap sebagai alur backend tempat Anda dapat mengotomatiskan tugas seperti menambahkan atau menghapus tag, menyetel variabel bidang khusus, melakukan panggilan API eksternal.

Dengan cara ini, percakapan Anda dengan pelanggan tidak akan terpengaruh oleh keharusan menunggu untuk menerapkan semua tindakan tersebut dan pengalaman semulus mungkin bagi pengguna akhir tersebut.

## Buat Alur Kerja
Untuk membuat alur kerja, buka ikhtisar alur dengan memilih Alur dari menu sebelah kiri.

Kemudian tekan tombol + Sub Flow Baru

[gambar]

Pilih jenis aliran alur kerja lalu beri nama. Setelah selesai tekan tombol Buat untuk mulai membuat alur kerja Anda.

Setelah Anda membuat aliran dan Anda berakhir di pembuat aliran, Anda akan melihat bahwa Anda akan memiliki akses ke lebih sedikit blok daripada saat memilih aliran reguler atau fungsi.

Blok yang tersedia adalah:

Tindakan
Kondisi
Membelah
Mengirim email
Seperti yang disebutkan, alur ini dimaksudkan untuk membuat aliran backend yang dapat Anda picu dari aliran lain di dalam chatbot Anda untuk menangani tugas sistem seperti menambahkan tag, menyetel bidang khusus, tetapi juga mengirim email.

[gambar]

## Contoh Alur Kerja
Mari kita ambil contoh bagaimana alur kerja dapat digunakan.

Seorang pengguna mendaftar dengan email dan atau nomor telepon dan Anda ingin menyinkronkan informasi ini dengan platform CRM pilihan Anda.

Segera setelah Anda mendapatkan kredensial dari pengguna, Anda dapat melakukan panggilan API menggunakan blok permintaan eksternal di dalam modul tindakan.

Anda juga ingin menandai pengguna di dalam chatbot untuk menyelesaikan langkah orientasi. Setelah selesai, kami mengirim email pemberitahuan ke admin bahwa prospek baru telah dibuat untuk ditindaklanjuti.

Alur kerja kemudian dapat terlihat seperti ini;

[gambar]

Jika Anda memasukkan ini ke dalam aliran yang memiliki percakapan sebenarnya, ini mungkin menjadi masalah karena percakapan dapat ditahan selama beberapa detik atau lebih untuk menyelesaikan semua proses sistem ini. Dan Anda mungkin kehilangan pengguna karena menurutnya percakapan sudah selesai.

## Pemicu Alur Kerja
Sangat mudah untuk memicu alur kerja di atas di dalam alur lain yang Anda buat.

Cukup masukkan blok tindakan, buka tindakan lanjutan, lalu pilih pemicu alur kerja di bagian bawah

[gambar]

Anda kemudian dapat memilih alur kerja apa pun yang Anda buat. Alur kerja ini kemudian akan diproses di backend sementara percakapan dengan pengguna tidak akan terpengaruh dan berlanjut tanpa penundaan.
