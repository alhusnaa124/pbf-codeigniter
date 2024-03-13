# AL HUSNAA NANDA KURNIA (220302025)

## Welcome to Codeigniter 4
CodeIgniter adalah sebuah toolkit untuk membangun situs web dengan PHP yang memungkinkan pengembangan proyek lebih cepat. Dengan menyediakan kumpulan perpustakaan untuk tugas umum dan antarmuka sederhana, CodeIgniter meminimalkan jumlah kode yang dibutuhkan. Fleksibilitasnya memungkinkan pengguna bekerja sesuai keinginan tanpa dipaksa mengikuti pola tertentu. Kerangka kerja ini dapat diperluas atau diganti sesuai kebutuhan, menjadikannya solusi lunak yang menyediakan alat tanpa mengganggu.
## Persyaratan Server
  ### PHP dan Ekstensi yang Diperlukan
  Diperlukan PHP versi 7.4 atau lebih baru, dengan ekstensi PHP berikut diaktifkan:
  - internasional
  - mbstring
  - json
  ### Ekstensi PHP Opsional
  1. Ekstensi PHP berikut harus diaktifkan di server Anda:
  - mysqlnd (jika Anda menggunakan MySQL)
    MySQL Native Driver (mysqlnd) adalah penggerak MySQL untuk PHP yang menyediakan antarmuka langsung dan efisien antara PHP dan server MySQL, memungkinkan kinerja dan penggunaan memori yang lebih baik daripada alternatifnya.
  - curl (jika Anda menggunakan CURLRequest )
    Curl (Client for URLs) adalah alat baris perintah dan perpustakaan untuk mentransfer data melalui berbagai protokol seperti HTTP, HTTPS, dan FTP, sering digunakan dalam skrip shell dan pengembangan web untuk berkomunikasi dengan server.
  - imagick (jika Anda menggunakan kelas Gambar ImageMagickHandler)
    imagick adalah sebuah ekstensi PHP yang memungkinkan manipulasi gambar, seperti resizing, cropping, rotasi, dan efek lainnya, menggunakan ImageMagick API
  - gd (jika Anda menggunakan kelas Gambar GDHandler)
    GD adalah pustaka perangkat lunak dalam PHP yang memungkinkan manipulasi gambar secara dinamis untuk keperluan pengembangan web.
  - simplexml (jika Anda memformat XML)
    SimpleXML adalah ekstensi PHP yang menyediakan cara mudah untuk mengurai dan membuat XML (eXtensible Markup Language) menggunakan antarmuka objek, memungkinkan manipulasi data XML dengan mudah dan intuitif dalam pengembangan aplikasi web dan layanan web.
    
  2. Ekstensi PHP berikut diperlukan saat Anda menggunakan server Cache:
     - memcache (jika Anda menggunakan kelas Cache MemcachedHandler dengan Memcache)
     - memcached (jika Anda menggunakan kelas Cache MemcachedHandler dengan Memcached)
     - redis (jika Anda menggunakan kelas Cache RedisHandler)
     
  4. Ekstensi PHP berikut diperlukan saat Anda menggunakan PHPUnit:
     - dom (jika Anda menggunakan kelas TestResponse )
       DOM (Document Object Model) adalah antarmuka pemrograman yang menyediakan cara untuk mengakses dan memanipulasi struktur dokumen HTML dan XML dalam pengembangan web.
     - libxml (jika Anda menggunakan kelas TestResponse )
       Libxml adalah perpustakaan yang digunakan dalam bahasa pemrograman PHP untuk mem-parsing dokumen XML dan menyediakan fungsi-fungsi untuk memanipulasi data XML.
     - xdebug (jika Anda menggunakan CIUnitTestCase::assertHeaderEmitted())
       Xdebug adalah ekstensi PHP yang menyediakan kemampuan debugging dan profil. Ini menggunakan protokol debugging DBGp.
       
  ### Basis Data yang Didukung
  **Basis data diperlukan untuk sebagian besar pemrograman aplikasi web. Basis data yang didukung saat ini adalah:**
  - MySQL melalui MySQLidriver (hanya versi 5.1 ke atas)
  - PostgreSQL melalui Postgredriver (hanya versi 7.4 dan lebih tinggi)
  - SQLite3 melalui SQLite3driver
  - Microsoft SQL Server melalui SQLSRVdriver (hanya versi 2005 dan lebih tinggi)
  - Oracle Database melalui OCI8driver (hanya versi 12.1 dan lebih tinggi)
  **Tidak semua driver telah dikonversi/ditulis ulang untuk CodeIgniter4. Daftar di bawah ini menunjukkan yang luar biasa.**
  - MySQL (5.1+) melalui driver pdo
  - Oracle melalui driver pdo
  - PostgreSQL melalui driver pdo
  - MSSQL melalui driver pdo
  - SQLite melalui sqlite (versi 2) dan driver pdo
  - CUBRID melalui driver cubrid dan pdo
  - Interbase/Firebird melalui driver ibase dan pdo
  - ODBC melalui driver odbc dan pdo (Anda harus tahu bahwa ODBC sebenarnya adalah lapisan abstraksi)

## Instalation
### Composer Instalation
CodeIgniter4 memerlukan Composer 2.0.14 atau lebih baru.
1. Ketikan Perintah di bawah ini pada CMD / Terminal, pastikan direktori sudah sesuai
   ```shell
   composer create-project codeigniter4/appstarter project-root
```
Perintah di atas akan membuat folder root proyek .
2. 
