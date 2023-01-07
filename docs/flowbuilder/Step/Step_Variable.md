# Action Step Variable Operation
UChat memberi Anda berbagai operasi bawaan untuk modifikasi variabel.

Ada 6 jenis variabel di UChat:

|   Type   |            Storage           |           Example           | Operation                                                                 |
|:--------:|:----------------------------:|:---------------------------:|---------------------------------------------------------------------------|
|   Text   | letters, words, sentences... |          Hi, UChat.         | cutting, change case, encode, decode...                                   |
|  Number  |            number            |            123.45           | + - x ÷, mod, power, log, root, round...                                  |
|  Boolean |     either "yes" or "no"     |             yes             | assign                                                                    |
|   Date   |             date             |          2021-03-30         | format, add months/weeks/days                                             |
| DateTime |         date and time        |     2021-03-30 16:52:00     | format, add months/weeks/days/hours/minutes                               |
|   JSON   |     a series of variables    | {"name":"jack", "age":"10"} | load, get, update, remove, count, sum, average, sort, shuffle, reverse... |

[gambar]

Klik "Tindakan Dasar" pada langkah Tindakan dan ini adalah "Tetapkan Nilai Variabel" dan "Hapus Nilai Variabel".

### Hapus Bidang Kustom / Hapus JSON
Untuk menghapus teks, angka, boolean, tanggal, variabel datetime, harap gunakan tindakan Hapus Bidang Kustom.

Untuk menghapus variabel JSON, harap gunakan operasi Hapus Semua Item di Operasi JSON.

### nilai input
Operasi "nilai input" digunakan untuk menetapkan nilai ke variabel. Operasi ini berfungsi untuk semua jenis variabel.

[gambar]

### Rumus Matematika

[gambar]

Dengan operasi ini, Anda sekarang dapat melakukan penghitungan rumus secara langsung di Langkah Tindakan - "Tetapkan Nilai Variabel" dan Langkah Ketentuan - "Nilai".

Operasi matematika dan fungsi yang didukung:

+, -, *, e, pi, PI, abs(), min(), maks(), ceil(), lantai(), log(), pow(), bulat(), sqrt(), sin( ), cos(), tan()

## Tetapkan Variabel Teks

### potong teks

|               Description              | e.g. Before | e.g. After |
|:--------------------------------------:|:-----------:|:----------:|
| remove spaces before or after the text |   " abc "   |    "abc"   |

[gambar]

### sub string

|      Description     |  e.g. Before | e.g. After |
|:--------------------:|:------------:|:----------:|
| get part of the text | "Hi, UChat!" |   "UChat"  |

[gambar]

[gambar]

### ganti string / ganti string case sensitive

|        Description       |  e.g. Before |    e.g. After   |
|:------------------------:|:------------:|:---------------:|
| replace part of the text | "Hi, UChat!" | "Hello, UChat!" |

[gambar]

[gambar]

### ke huruf kecil/besar

|      Type     |  e.g. Before |  e.g. After  |
|:-------------:|:------------:|:------------:|
| to lower case | "Hi, UChat!" | "hi, uchat!" |
| to upper case | "Hi, UChat!" | "HI, UCHAT!" |

[gambar]

### menghasilkan teks acak

| Description |       e.g. Before      |       e.g. After       |
|:-----------:|:----------------------:|:----------------------:|
| as the name | "code: XXXX-####-xxxx" | "code: UBWT-3657-lkzb" |

[gambar]

Fitur ini berguna saat Anda perlu membuat kode verifikasi atau kode referensi satu kali.

### url menyandikan / mendekode

|  Type  |    e.g. Before   |    e.g. After    |
|:------:|:----------------:|:----------------:|
| encode |   "Hi, UChat!"   | "Hi%2C%20UChat!" |
| decode | "Hi%2C%20UChat!" |   "Hi, UChat!"   |

[gambar]

### penyandian / dekode base64

| Description |     e.g. Before    |     e.g. After     |
|:-----------:|:------------------:|:------------------:|
|    encode   |    "Hi, UChat!"    | "SGksIFVDaGF0IQ==" |
|    decode   | "SGksIFVDaGF0IQ==" |    "Hi, UChat!"    |

[gambar]

### to URL friendly slugs

|                      Description                      |    e.g. Before    |    e.g. After    |
|:-----------------------------------------------------:|:-----------------:|:----------------:|
| replace spaces with hyphens and remove the rest signs | "it's a good day" | "its-a-good-day" |

[gambar]

### get text before/after ...
Description: get part of the text.

|                    Type                    |          e.g. Before         |       e.g. After       |
|:------------------------------------------:|:----------------------------:|:----------------------:|
|        get text before another text        | name: UChat, city: Melbourne |          name          |
| get text before last occur of another text | name: UChat, city: Melbourne |    name: UChat, city   |
|         get text after another text        | name: UChat, city: Melbourne | UChat, city: Melbourne |
|  get text after last occur of another text | name: UChat, city: Melbourne |        Melbourne       |

[gambar]

## Set Number Variables

### get textlength

| Description | e.g. Before | e.g. After |
|:-----------:|:-----------:|:----------:|
| as the name |    500.59   |      6     |

[gambar]

### generate random number

| Description | e.g. Before | e.g. After |
|:-----------:|:-----------:|:----------:|
| as the name |     n/a     |     56     |

[gambar]

### add / subtract / multiply / divide / modulus / power / natural logarithm / square root

| Description | e.g. Before | e.g. After |
|:-----------:|:-----------:|:----------:|
| as the name |      7      |      8     |

[gambar]

### round

| Description | e.g. Before | e.g. After |
|:-----------:|:-----------:|:----------:|
| as the name |    7.8693   |    7.87    |

[gambar]

### floor / ceiling
Description: get approximate integer.

|  Type | e.g. Before | e.g. After |
|:-----:|:-----------:|:----------:|
| floor |     6.55    |      6     |
|  ceil |     6.55    |      7     |

[gambar]

## Set DateTime Variable

### from formatted text

|               Description              |       e.g. Before       |      e.g. After     |
|:--------------------------------------:|:-----------------------:|:-------------------:|
| get DataTime value from formatted text | 00:00:00 30th Aug, 2020 | 2020-08-30 00:00:00 |

[gambar]

### add minutes / hours / days / weeks / months

| Description |     e.g. Before     |      e.g. After     |
|:-----------:|:-------------------:|:-------------------:|
| as the name | 2021-01-01 00:00:00 | 2021-01-01 00:01:00 |

[gambar]













