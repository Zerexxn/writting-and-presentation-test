# Week 5 [Back-End Bootcamp]
## Tugas Writing & Presentation test Week 5

&nbsp;

## *Web Server & RESTful API*
### *Web Server*
Web server terdiri dari 2 komponen penting yaitu software dan hardware. Di sisi hardware berfungsi untuk menyimpan web server software dan komponen file website seperti HTML, CSS, dan JS. Di sisi software terdapat HTTP server yang memahami alamat website dan HTTP.

### *Restful API*
RESTful API / REST API merupakan penerapan dari API (Application Programming Interface). 

Sedangkan REST (Representional State Transfer) adalah sebuah arsitektur metode komunikasi yang menggunakan protokol HTTP untuk pertukaran data dimana metode ini sering diterapkan dalam pengembangan aplikasi. Dengan tujuannya untuk menjadikan sistem memiliki performa yang baik, cepat dan mudah untuk di kembangkan (scale) terutama dalam pertukaran dan komunikasi data.

Software Architecture:
- the monolith
- front & back
- microservices

HTTP Methode:
- get     (mendapatkan data)
- post    (mengirim/tambah data baru)
- delete  (hapus data)
- put     (mengupdate data)
- path (partial) -> endpoint alamat url 

Status Code:
- 1xx -> informational
- 2xx -> success
- 3xx -> redirection
- 4xx -> client error, kesalahan pada usernya (halaman tidak tersedia)
- 5xx -> server error, kesalahan pada server

ambil semua data: /user-devices;
ambil data berdasarkan id ke-3(path): /user-devices/3

&nbsp;

## *Intro Node.Js*
Node JS merupakan open source dan back end JavaScript runtime environment yang berjalan di V8 engine dan mengeksekusi JavaScript di luar Web Browser. Node JS sendiri berguna untuk menjalankan script server side yang membuat website menjadi dinamis.
### *Module JavaScript yang dipakai*
  - `console`, digunakan sebagai debug
  - `process`, digunakan untuk menampilkan dan mengontrol process di node.js
  - `os`, digunakan untuk memberikan informasi mengenai sistem operasi komputer
  - file system (`fs`), digunakan untuk berinteraksi dengan file yang ada di luar code
  - `util`, digunakan untuk kebutuhan API di node js
  errors, digunakan untuk mendefinisikan error
buffer, digunakan untuk mengakses tipe data bytes dan raw
  - `timers`, digunakan untuk mengatur sebuah waktu
  - `events`
  - `app`

&nbsp;

## *Express Js*
Express.js, atau biasa disebutExpress, adalah sebuah open-source, cross-platform, `back-end JavaScript runtime` environment sebagai perangkat lunak bebas di bawah Lisensi MIT. Dirancang untuk membangun aplikasi web dan API.

`Back-End app` adalah aplikasi yang berjalan di server-side yang bekerja untuk memberikan informasi berupa data sesuai request dari client / browser / front end app. Umumnya server-side app membuat REST API.

4 komponen penting pada Restful API:
- URL Design
- HTTP Verbs
- HTTP Response Code
- Format Response

### *Routing* -- Routing merupakan manajemen endpoint dari sebuah aplikasi atau website untuk melakukan request dan memberikan response oleh client.

### *Middleware* -- Middleware merupakan fungsi yang terdiri dari 3 parameter yaitu req (untuk mendapatkan data), res (memberikan response), dan next (untuk melanjutkan ke route lain yang berhubungan).

&nbsp;

## *Design Database with MySQL*
- Membuat Diagram Entity
- Menentukan Atribut Entity
- Menentukan dan Membuat Relasi Entity
### *Menentukan Entity dan Atribbutes*
Beberapa kandidat yang paling sering menjadi sebuah entity : `peoples`, `things`, `events`, `locations`.

Berikut kandidat yang bisa dijadikan enitity dalam database :
- User
- Singer
- Track
- Album
- Playlist

Attributes yang di perlukan didalam entity kemungkinan sudah ada di dalam requirements document, atau mungkin juga diperlukan penafsiran kita sendiri sebagai database developer.
