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
2. pindah direktori ke file yang telah di buat
  ```shell
  cd project-root
  ```
2. Upgrade
  Setiap kali ada rilis baru, maka dari baris perintah di root proyek Anda:
  ```shell
  composer update
  ```
3. Update for Latest Dev
   memperbarui composer.json agar menunjuk ke developcabang repositori yang berfungsi, dan memperbarui jalur terkait di file konfigurasi dan XML.
   ```shell
   php builds development
   ```
4. Revert to Stable Release
   Untuk mengembalikan perubahan, jalankan:
   ```shell
   php builds release
   ```
**Kelebihan**
Instalasi sederhana; mudah untuk diperbarui.
**Kontra**
Anda masih perlu memeriksa perubahan file di ruang proyek (root, aplikasi, publik, dapat ditulisi) dan menggabungkannya setelah memperbarui.
**Struktur**
Folder di proyek Anda setelah pengaturan:
aplikasi, publik, tes, dapat ditulis
vendor/codeigniter4/framework/system

### Manual Instalation
1. Unduh [versi terbaru](https://github.com/CodeIgniter4/framework/releases/tag/v4.4.6) , dan ekstrak untuk menjadi root proyek Anda.
2. ketika link di buka scroll kebawah sampai asset, pilih Source code yang zip.
3. setelah Berhasil di download , ekstrak file tersebut
**Kelebihan**
Unduh dan jalankan.
**Kontra**
Anda perlu memeriksa perubahan file di ruang proyek (root, aplikasi, publik, pengujian, dapat ditulisi) dan menggabungkannya sendiri.
**Struktur**
Folder di proyek Anda setelah pengaturan:
aplikasi, publik, tes, dapat ditulis, sistem

### Local Development Server
untuk menjalankan codeigniter, dapat menggunakan baris perintah berikut di direktori file project yang telah di buat:
```shell
php spark serve
```
Ini akan meluncurkan server dan sekarang Anda dapat melihat aplikasi Anda di browser Anda di http://localhost:8080 .

**Server pengembangan lokal dapat dikustomisasi dengan tiga opsi baris perintah:**
- Anda dapat menggunakan --hostopsi CLI untuk menentukan host berbeda untuk menjalankan aplikasi di:
  ```shell
  php spark serve --host example.dev
  ```
- Secara default, server berjalan pada port 8080 tetapi Anda mungkin menjalankan lebih dari satu situs, atau sudah memiliki aplikasi lain yang menggunakan port tersebut. Anda dapat menggunakan --portopsi CLI untuk menentukan opsi lain:
  ```shell
  php spark serve --port 8081
  ```
- Anda juga dapat menentukan versi PHP tertentu yang akan digunakan, dengan --phpopsi CLI, dengan nilainya disetel ke jalur eksekusi PHP yang ingin Anda gunakan:
  ```shell
  php spark serve --php /usr/bin/php7.6.5.4
  ```

  ## Build Your First Application
  ### Static Page
  1. Menetapkan Aturan Perutean
     Perutean mengaitkan URI dengan metode pengontrol
     Buka file rute yang terletak di app/Config/Routes.php
     ```shell
     <?php
     use CodeIgniter\Router\RouteCollection;
     /**
     * @var RouteCollection $routes
     */
     $routes->get('/', 'Home::index');
     ```
     Tambahkan baris berikut, setelah arahan rute untuk '/'
     ```shell
     use App\Controllers\Pages;
     $routes->get('pages', [Pages::class, 'index']);
     $routes->get('(:segment)', [Pages::class, 'view']);
     ```
     CodeIgniter membaca aturan routingnya dari atas ke bawah dan merutekan permintaan ke aturan pertama yang cocok. Setiap aturan adalah ekspresi reguler (sisi kiri) yang dipetakan ke pengontrol dan nama metode (sisi kanan).
     Di sini, aturan kedua dalam $routes objek mencocokkan permintaan GET dengan jalur URI /pages , dan dipetakan ke index()metode kelas Pages. Aturan ketiga dalam $routes objek mencocokkan permintaan GET ke segmen URI menggunakan placeholder (:segment), dan meneruskan parameter ke view()metode kelas Pages.
  2. Buat Pengontrol Halaman
     Buat file di app/Controllers/Pages.php dengan kode berikut:
     ```shell
     <?php
     namespace App\Controllers;
     class Pages extends BaseController
     {
       public function index()
      {
        return view('welcome_message');
      }
      public function view($page = 'home')
      {
        // ...
      }
    }
    ```
    Anda telah membuat kelas bernama Pages, dengan view()metode yang menerima satu argumen bernama $page. Ia juga memiliki index()metode, sama dengan pengontrol default yang ditemukan di app/Controllers/Home.php ; metode itu menampilkan halaman selamat datang CodeIgniter.
  3. Buat Tampilan
    - Buat header di app/Views/templates/header.php dan tambahkan kode berikut:
      ```shell
      <!doctype html>
      <html>
      <head>
        <title>CodeIgniter Tutorial</title>
      </head>
      <body>
      <h1><?= esc($title) ?></h1>
      ```
    - Buat footer di app/Views/templates/footer.php dan tambahkan kode berikut:
      ```shell
          <em>&copy; 2022</em>
      </body>
      </html>
      ```
  4. Halaman Lengkap::view() Metode
    di app/Controllers/Pages.php
    ```shell
    <?php
    namespace App\Controllers;
    use CodeIgniter\Exceptions\PageNotFoundException; // Add this line
    class Pages extends BaseController
    {
        // ...

      public function view($page = 'home')
        {
          if (! is_file(APPPATH . 'Views/pages/' . $page . '.php')) {
            // Whoops, we don't have a page for that!
            throw new PageNotFoundException($page);
        }
        $data['title'] = ucfirst($page); // Capitalize the first letter

        return view('templates/header', $data)
            . view('pages/' . $page)
            . view('templates/footer');
      }  
    }
   ```
  Jalankan untuk mengecek hasil yang sudah di buat dengan code:
  ```shell
  php spark serve
  ``` 
### News Section
1. Buat Database untuk Digunakan
    jalankan perintah SQL di bawah ini di php my admin atau yang lainnya:
   ```shell
     CREATE TABLE news (
      id INT UNSIGNED NOT NULL AUTO_INCREMENT,
      title VARCHAR(128) NOT NULL,
      slug VARCHAR(128) NOT NULL,
      body TEXT NOT NULL,
      PRIMARY KEY (id),
      UNIQUE slug (slug)
  );
  ```
2. Isikan Data dengan perintah :
```shell
    INSERT INTO news VALUES
  (1,'Elvis sighted','elvis-sighted','Elvis was sighted at the Podunk internet cafe. It looked like he was writing a CodeIgniter app.'),
  (2,'Say it isn\'t so!','say-it-isnt-so','Scientists conclude that some programmers have a sense of humor.'),
  (3,'Caffeination, Yes!','caffeination-yes','World\'s largest coffee shop open onsite nested coffee shop for staff only.');
```
3. Hubungkan ke Basis Data Anda
   - buka visual studio code atau teks editor lainnya
   - kemudian cari file .env , jika masih env maka rename menjadi .env
   - kemudian cari kode berikut:
     ```shell
      database.default.hostname = localhost
      database.default.database = ci4tutorial
      database.default.username = root
      database.default.password = 
      database.default.DBDriver = MySQLi
     ```
  - hapus tanda # untuk menonaktifkan komentar, kemudian sesuaikan isinya.
4. Buat Model Berita
  Buka direktori app/Models dan buat file baru bernama NewsModel.php dan tambahkan kode berikut:
  ```shell
  <?php
  namespace App\Models;
  use CodeIgniter\Model;
  class NewsModel extends Model
  {
      protected $table = 'news';
  }
  ```
5. Tambahkan Metode NewsModel::getNews()
   buka file di app/Models/NewsModel.php
   tambahkan method
   ```shell
   public function getNews($slug = false)
    {
        if ($slug === false) {
            return $this->findAll();
        }
        return $this->where(['slug' => $slug])->first();
    }
   ```
6. Menambahkan Aturan Perutean
   Ubah file app/Config/Routes.php
   ```shell
   <?php
    // ...
    use App\Controllers\News; // Add this line
    use App\Controllers\Pages;
    
    $routes->get('news', [News::class, 'index']);           // Add this line
    $routes->get('news/(:segment)', [News::class, 'show']); // Add this line
    
    $routes->get('pages', [Pages::class, 'index']);
    $routes->get('(:segment)', [Pages::class, 'view']);
  ```
7. Buat Pengontrol Berita
   Buat pengontrol baru di app/Controllers/News.php
   ```shell
       <?php
    namespace App\Controllers;
    use App\Models\NewsModel;
    class News extends BaseController
    {
        public function index()
        {
            $model = model(NewsModel::class);
    
            $data['news'] = $model->getNews();
        }
    
        public function show($slug = null)
        {
            $model = model(NewsModel::class);
    
            $data['news'] = $model->getNews($slug);
        }
    }
  ```
8. Berita Lengkap::index() Metode
   ```shell
   <?php
      namespace App\Controllers;
      
      use App\Models\NewsModel;
      
      class News extends BaseController
      {
          public function index()
          {
              $model = model(NewsModel::class);
      
              $data = [
                  'news'  => $model->getNews(),
                  'title' => 'News archive',
              ];
      
              return view('templates/header', $data)
                  . view('news/index')
                  . view('templates/footer');
          }
      
          // ...
      }
   ```
9. Buat File Tampilan berita/indeks
   Buat app/Views/news/index.php dan tambahkan potongan kode berikutnya.
  ```shell
  <h2><?= esc($title) ?></h2>
  
  <?php if (! empty($news) && is_array($news)): ?>
  
      <?php foreach ($news as $news_item): ?>
  
          <h3><?= esc($news_item['title']) ?></h3>
  
          <div class="main">
              <?= esc($news_item['body']) ?>
          </div>
          <p><a href="/news/<?= esc($news_item['slug'], 'url') ?>">View article</a></p>
  
      <?php endforeach ?>
  
  <?php else: ?>
  
      <h3>No News</h3>
  
      <p>Unable to find any news for you.</p>
  
  <?php endif ?>
  ```
10. Berita Lengkap::show() Metode
    ```shell
    <?php

    namespace App\Controllers;
    
    use App\Models\NewsModel;
    use CodeIgniter\Exceptions\PageNotFoundException;
    
    class News extends BaseController
    {
        // ...
    
        public function show($slug = null)
        {
            $model = model(NewsModel::class);
    
            $data['news'] = $model->getNews($slug);
    
            if (empty($data['news'])) {
                throw new PageNotFoundException('Cannot find the news item: ' . $slug);
            }
    
            $data['title'] = $data['news']['title'];
    
            return view('templates/header', $data)
                . view('news/view')
                . view('templates/footer');
        }
    }
    ```
11. Buat berita/lihat Lihat File
    membuat tampilan terkait di app/Views/news/view.php , masukan kode berikut :
  ```shell
  <h2><?= esc($news['title']) ?></h2>
  <p><?= esc($news['body']) ?></p>
 ```
12. kemudian jalankan
    Arahkan browser Anda ke halaman “berita”, yaitu localhost:8080/news

### Codeigniter 4 Overview
## Models, Views, and Controllers
MVC adalah Setiap aplikasi memerlukan pengaturan kode yang baik untuk pemeliharaan, dan CodeIgniter menggunakan pola Model, View, Controller (MVC) untuk memisahkan data, presentasi, dan logika aplikasi
**Model** mengelola data aplikasi dan membantu menegakkan aturan bisnis khusus yang mungkin diperlukan aplikasi.

**Tampilan** adalah file sederhana, dengan sedikit atau tanpa logika, yang menampilkan informasi kepada pengguna.

**Pengontrol** bertindak sebagai kode perekat, menyusun data bolak-balik antara tampilan (atau pengguna yang melihatnya) dan penyimpanan data.
Komponen
**View**
Tampilan dalam CodeIgniter adalah file HTML yang sederhana dengan sedikit kode PHP untuk menampilkan konten variabel atau mengulang item dalam tabel. Data untuk tampilan diteruskan dari pengontrol sebagai variabel yang ditampilkan dengan panggilan echo. Anda juga dapat menyertakan tampilan lain dalam tampilan, seperti header atau footer, untuk memudahkan penggunaan umum. Meskipun umumnya disimpan di direktori app/Views, aturan praktis yang baik adalah membuat direktori baru untuk setiap pengontrol dan menamai file tampilan berdasarkan nama metode, yang membuatnya mudah ditemukan. Meskipun tidak ada aturan baku untuk organisasi file tampilan, penting untuk mengatur mereka dengan cara yang mudah dipahami dan diakses.
**Model**
Tugas model adalah mengelola satu jenis data untuk aplikasi, termasuk menerapkan aturan bisnis pada data dari database dan menangani penyimpanan serta pengambilan data. Aturan bisnis, seperti normalisasi atau pemformatan data, diterapkan dalam model untuk mencegah pengulangan kode di berbagai pengontrol. Model biasanya disimpan di direktori app/Models dengan kemungkinan penggunaan namespace untuk pengelompokan.
**Controller**
Pengendali bertanggung jawab atas menerima masukan dari pengguna dan menentukan tindakan yang harus diambil, termasuk menyimpan atau meminta data dari model, serta memuat kelas utilitas tambahan. Mereka juga menangani aspek permintaan HTTP seperti pengalihan, otentikasi, dan keamanan web, serta memastikan bahwa pengguna diizinkan berada di sana dan mendapatkan data dalam format yang sesuai. Pengendali biasanya disimpan di direktori app/Controllers dengan kemungkinan penggunaan namespace untuk pengelompokan yang lebih baik.

## General Topic
### Helper Function
Helper dalam CodeIgniter adalah kumpulan fungsi prosedural dalam berbagai kategori seperti URL, Formulir, Tes, Cookie, dan Sistem File, yang membantu dalam tugas-tugas tertentu tanpa ketergantungan pada fungsi lainnya. Mereka tidak ditulis dalam format Berorientasi Objek dan harus dimuat secara eksplisit sebelum digunakan, setelah itu tersedia secara global di pengontrol dan tampilan. Helper biasanya disimpan di direktori sistem/Helpers atau app/Helpers.
1. create Helper
   Kode di bawah memuat file name_helper.php
   ```shell
   <?php
   helper('name');
   ```
   Misalnya, untuk memuat file Cookie Helper , yang diberi nama cookie_helper.php , Anda akan melakukan ini:
  ```shell
  <?php
  helper('cookie');
  ```
2. Load Order
   Fungsi `helper()` memindai seluruh namespace yang ditentukan dan memuat semua helper yang cocok dengan nama yang sama, memungkinkan untuk memuat helper dari modul apa pun dan juga helper yang dibuat khusus untuk aplikasi ini.
   Urutan pemuatannya adalah sebagai berikut:
   - app/Helpers - File yang dimuat di sini selalu dimuat terlebih dahulu.
   - {namespace}/Helpers - Semua namespace diulang sesuai urutan yang ditentukan.
   - system/Helpers - File dasar dimuat terakhir.

3. Loading Multiple Helpers
   Jika Anda perlu memuat lebih dari satu helper sekaligus, Anda dapat meneruskan serangkaian nama file dan semuanya akan dimuat:
   ```shell
   <?php
    helper(['cookie', 'date']);
   ```
4. Loading in Controller
   Helper dapat dimuat di mana saja dalam metode pengontrol Anda (atau bahkan dalam file View Anda, meskipun itu bukan praktik yang baik), selama Anda memuatnya sebelum menggunakannya.
5. Loading from Specified Namespace
   Jika Anda hanya ingin memuat helper di namespace tertentu, awali nama helper dengan namespace tempatnya berada.
   Di dalam pengontrol kita, kita dapat menggunakan perintah berikut untuk memuat helper untuk kita:
   ```shell
   <?php 
    helper('App\Helpers\contoh');
6. Membuat Helper Khusus
   Nama file pembantu adalah nama pembantu dan _helper.php .
    Misalnya, untuk membuat info helper, Anda akan membuat file bernama app/Helpers/info_helper.php , dan menambahkan fungsi ke file
   ```shell
   <?php

    // app/Helpers/info_helper.php
    use CodeIgniter\CodeIgniter;
    
    /**
     * Returns CodeIgniter's version.
     */
    function ci_version(): string
    {
        return CodeIgniter::CI_VERSION;
    }
   ```
7. “Extending” Helpers
   Untuk “memperluas” Helper, buat file di folder aplikasi/Helpers Anda dengan nama yang sama dengan Helper yang ada.
   Misalnya, untuk memperluas Array Helper asli,  akan membuat file bernama app/Helpers/array_helper.php ,
   ```shell
   <?php
    
    // any_in_array() is not in the Array Helper, so it defines a new function
    function any_in_array($needle, $haystack)
    {
        $needle = is_array($needle) ? $needle : [$needle];
    
        foreach ($needle as $item) {
            if (in_array($item, $haystack, true)) {
                return true;
            }
        }
    
        return false;
    }
    // random_element() is included in Array Helper, so it overrides the native function
    function random_element($array)
    {
        shuffle($array);
        return array_pop($array);
    }
   ```
## Controllers and Routing
### Controllers
Pengontrol dalam aplikasi web adalah bagian dari pola desain MVC yang bertanggung jawab untuk menerima permintaan dari pengguna, memprosesnya, dan menghasilkan respon yang sesuai.Dalam CodeIgniter, pengontrol biasanya disimpan dalam direktori app/Controllers.
1. Constructor
   Controller CodeIgniter memiliki konstruktor khusus initController(). Ini akan dipanggil oleh framework setelah __construct()eksekusi konstruktor PHP.
   ```shell
   <?php

    namespace App\Controllers;
    
    use CodeIgniter\HTTP\RequestInterface;
    use CodeIgniter\HTTP\ResponseInterface;
    use Psr\Log\LoggerInterface;
    
    class Product extends BaseController
    {
        public function initController(
            RequestInterface $request,
            ResponseInterface $response,
            LoggerInterface $logger
        ) {
            parent::initController($request, $response, $logger);
    
            // Add your code here.
        }
    
        // ...
    }
   ```
2. Helpers
   Mendefinisikan array file pembantu sebagai properti kelas. Setiap kali pengontrol dimuat, file helper ini akan secara otomatis dimuat ke dalam memori sehingga Anda dapat menggunakan metodenya di mana saja di dalam pengontrol:
   ```shell
   <?php
  
  namespace App\Controllers;
  
  class MyController extends BaseController
  {
      protected $helpers = ['url', 'form'];
  }
  ```
3. forceHTTPS
  Metode praktis untuk memaksa suatu metode diakses melalui HTTPS tersedia di semua pengontrol:
  ```shell
  <?php
  
  if (! $this->request->isSecure()) {
      $this->forceHTTPS();
  }
  ```
Secara default, dan di browser modern yang mendukung header HTTP Strict Transport Security, panggilan ini akan memaksa browser untuk mengonversi panggilan non-HTTPS menjadi panggilan HTTPS selama satu tahun. Anda dapat mengubahnya dengan meneruskan durasi (dalam detik) sebagai parameter pertama:
```shell
<?php

if (! $this->request->isSecure()) {
    $this->forceHTTPS(31536000); // one year
}
```
4. Validasi Data
   pada app/Config/Validation.php
  ```shell
  <?php

    namespace App\Controllers;
    
    class UserController extends BaseController
    {
        public function updateUser(int $userID)
        {
            if (! $this->validate('userRules')) {
                // The validation failed.
                return view('users/update', [
                    'errors' => $this->validator->getErrors(),
                ]);
            }
    
            // The validation was successful.
    
            // Get the validated data.
            $validData = $this->validator->getValidated();
    
            // ...
        }
    }
  ```
5. contoh
   buat file helloworld.php di app\Controllers
   ```shell
   <?php

  namespace App\Controllers;
  
  class Helloworld extends BaseController
  {
      public function getIndex()
      {
          return 'Hello World!';
      }
  }
  ```
6. kemudian jalankan
7. Metode Biasa
  tambahkan method getComment di dalam file helloworld.php
  ```shell
  <?php
  namespace App\Controllers;
  
  class Helloworld extends BaseController
  {
      public function getIndex()
      {
          return 'Hello World!';
      }
  
      public function getComment()
      {
          return 'I am not flat!';
      }
  }
  ```
8. Mendefinisikan Pengontrol Default
  Mari kita coba dengan pengontrolnya Helloworld.
  Untuk menentukan pengontrol default, buka file app/Config/Routing.php Anda dan atur properti ini:
  ```shell
  public string $defaultController = 'Helloworld';
  ```
  Dimana Helloworld nama kelas pengontrol yang ingin Anda gunakan.
  Dan beri komentar pada baris di app/Config/Routes.php :
  ```shell
  $routes->get('/', 'Home::index');
  ```
9. Remapping Method Calls
    ```shell
    <?php
    
    namespace App\Controllers;
    
    class Products extends BaseController
    {
        public function _remap($method, ...$params)
        {
            $method = 'process_' . $method;
    
            if (method_exists($this, $method)) {
                return $this->{$method}(...$params);
            }
    
            throw \CodeIgniter\Exceptions\PageNotFoundException::forPageNotFound();
        }
    }
    ```
## Building Response
### Views
1. Membuat Tampilan
  Buat file dengan nama blog_view.php di app\Views
  ```shell
  <html>
      <head>
          <title>My Blog</title>
      </head>
      <body>
          <h1>Welcome to my Blog!</h1>
      </body>
  </html>
  ```
2. Menampilkan Tampilan
  Sekarang, buat file bernama Blog.php di direktori app/Controllers , dan letakkan ini di dalamnya:
  ```shell
    <?php
    
    namespace App\Controllers;
    
    class Blog extends BaseController
    {
        public function index()
        {
            return view('blog_view');
        }
    }
  ```
Buka file perutean yang terletak di app/Config/Routes.php :
```shell
use App\Controllers\Blog;
$routes->get('blog', [Blog::class, 'index']);
```
3. memuat banyak tampilan
   ```shell
  <?php
  
  namespace App\Controllers;
  
  use CodeIgniter\Controller;
  
  class Page extends Controller
  {
      public function index()
      {
          $data = [
              'page_title' => 'Your title',
          ];
  
          return view('header')
              . view('menu')
              . view('content', $data)
              . view('footer');
      }
  }
  ```
4. Menambahkan Data Dinamis ke Tampilan
  Data diteruskan dari pengontrol ke tampilan melalui array di parameter kedua fungsi view(). Berikut ini contohnya:
  ```shell
  <?php

  namespace App\Controllers;
  
  class Blog extends BaseController
  {
      public function index()
      {
          $data['title']   = 'My Real Title';
          $data['heading'] = 'My Real Heading';
  
          return view('blog_view', $data);
      }
  }
  ```
  Sekarang buka file view dan ubah teks menjadi variabel yang sesuai dengan kunci array di data Anda:
  ```shell
  <html>
      <head>
          <title><?= esc($title) ?></title>
      </head>
      <body>
          <h1><?= esc($heading) ?></h1>
      </body>
  </html>
  ```
5. Opsi Simpan Data
  ```shell
    $data = [
      'title'   => 'My title',
      'heading' => 'My Heading',
      'message' => 'My Message',
  ];
  
  return view('blog_view', $data, ['saveData' => false]);
  ```
6. Membuat Loop
   Berikut ini contoh sederhananya. Tambahkan ini ke pengontrol Anda:
  ```shell
  <?php
  
  namespace App\Controllers;
  
  class Blog extends BaseController
  {
      public function index()
      {
          $data = [
              'todo_list' => ['Clean House', 'Call Mom', 'Run Errands'],
              'title'     => 'My Real Title',
              'heading'   => 'My Real Heading',
          ];
  
          return view('blog_view', $data);
      }
  }
  ```
Sekarang buka file view Anda dan buat lingkaran:
```shell
<html>
<head>
    <title><?= esc($title) ?></title>
</head>
<body>
    <h1><?= esc($heading) ?></h1>

    <h2>My Todo List</h2>

    <ul>
    <?php foreach ($todo_list as $item): ?>

        <li><?= esc($item) ?></li>

    <?php endforeach ?>
    </ul>

</body>
</html>
```
