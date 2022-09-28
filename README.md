# writting-and-presentation-test week 1
## Day 1 : Apa itu CLI ?
### Unix Command Line 
 - **Shell** adalah sebuah program utama untuk berinteraksi dengan Sistem Operasi.
  - **Command Line Interface** adalah tampilan sebuah terminal yang digunakan untuk menjalankan program, mengelola file, dan berinteraksi dengan komputer. 
    - Bash
    - SH
    - CMD
    - Zsh
  - Cara membuka CLI 
    -  Buka menu pencarian pada Windows Logo 
    -  Ketikan “Git Bash” 
    -  Pilih Git Bash.

### Navigasi Menggunakan CLI
  - File System berfungsi untuk mengatur bagaimana data disimpan didalam sebuah sistem
    - ``ls`` digunakan untuk melihat isi file yang ada pada sebuah direktori
    - ``pwd`` digunakan untuk melihat current working direktori
    - ``cd`` <direktori> digunakan untuk berpindah direktor
   
### Manupulasi File dan Directory
  - ``mkdir`` membuat direktori baru.
   - ``touch`` membuat file baru.
  - ``cat`` melihat isi keseluruhan file.
  - ``head`` melihat isi awal file.
  - ``tail`` melihat isi akhir file.
  - ``cat`` melihat isi keseluruhan file.
  - ``cp`` mengcopy File, ``cp -R`` mengcopy direktori
  - ``mv`` memindahkan file/direktori, bia juga untuk mengganti nama file/direktori.
  - ``rm`` menghapus file, ``rm -R`` menghapus direktori
  
### Git & Github
  - *GIT* adalah sebuah tools bagi para programmer dan developer yang berfungsi sebagai control system untuk menjalankan proyek pengembangan software.
  - *Github* adalah platform atau layanan web host yang memungkinkan tim developer untuk bekerja bersama secara online

### Penggunaan GIT
  - ``$ git config --global user.name`` untuk melakukan konfigurasi username.
  - ``$ git config --global user.email`` untuk melakukan konfigurasi email.
  - ``$ git config --list`` untuk memastikan proses login berhasil.
  - ``$ git init`` digunakan untuk membuat repository di file lokal.
  - ``$ git status`` digunakan untuk mengetahui sebuah status dari sebuah repository.
  - ``$ git add`` menambahkan file baru pada repository yang dipilih.
  - ``$ git commit -m "first commit"`` untuk menyimpan perubahan yang dilakukan, tetapi tidak ada perubahan pada remote repository
  - ``$ git branch -m main`` untuk menggunakan branch main di repository
  - ``$ git remote add origin`` untuk menghubungkan remote repository dengan project lokal yang telah kita buat direktorinya
  - ``$ git push -u origin main`` untuk mengirimkan perubahan file setelah di commit ke remote repository
  - ``git checkout`` untuk menukar branch yang aktif dengan branchyang dipilih
  - ``git clone`` untuk membuat salinan repository lokal
  - ``git log`` untuk melihat catatan log perubahan pada respositori
  - ``git pull`` mengambil commit terbaru lalu otomatis menggabungkan (merge) dengan branch yang aktif
  
### Membuat Repository di Github
  - Login atau Register ke https://github.com/
  - Create New Repository
  - Isikan seperti nama Repository dan Deskripsi lalu Create Repository
  - Repository berhasil dibuat!

## Day 2 : HTML Dasar
### HTML : Hypertext Markup Language
  - HTML berfungsi untuk menampilkan konten pada browser
  - Tools yang digunakan untuk membuat HTML
    - Browser (Chrome)
    - Code Editor (Visual Studio Code)
  - HTML Structure

  ``` 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body></body>
</html>
```
  > Dokumen HTML harus memiliki struktur dasar yang terdiri dari 4 bagian utama yaitu: tag ``<!DOCTYPE>``, tag ``<html>``, tag ``<head>``, dan tag ``<body>``. dari Keempat bagian tersebut adalah syarat minimal yang menjadi standar pada struktur global dokumen HTML
  
  - Tag dasar pada HTML : 
    - Single Tag
      > Contoh : ``</br>``
    - Double Tag
      > Contoh : ``<p>``  ``</p>``
    - Comment Tag 
      > - digunakan untuk memberikan informasi tambahan pada kode HTML dan tidak jarang juga digunakan untuk menon-aktifkan beberapa kode HTML serta dapat menjadi pembatas antara code
      > - ``<!-- -->``

  - Contoh membuat tabel menggunakan *HTML*
 ``` 
<table border="1">
        <thead>
            <tr>
                <td>Nama</td>
                <td>Umur</td>
                <td>Jurusan</td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Dustin Bayu Herlambang</td>
                <td>20 Tahun</td>
                <td>Teknik Informatika</td></tf>
            </tr>
        </tbody>
    </table>
</html>
```

  - Output
  <table border="1">
        <thead>
            <tr>
                <td>Nama</td>
                <td>Umur</td>
                <td>Jurusan</td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Dustin Bayu Herlambang</td>
                <td>20 Tahun</td>
                <td>Teknik Informatika</td></tf>
            </tr>
        </tbody>
    </table>
 
  > - ``<thead>`` digunakan untuk membungkus konten bagian judul atau kepala tabel
  > - ``<tr>`` berfungsi untuk membuat baris pada tabel
  > - ``<td>`` digunakan untuk membuat kolom atau sel di setiap baris pada tabel
  > - ``<tbody>`` digunakan untuk membungkus konten bagian isi atau tubuh dari tabel
  
  - **Semantic Tag**
    > - Semantic Tag atau Semantic Markup, adalah sebutan untuk tag-tag HTML yang memiliki 'arti' atau 'makna'.
       > - Contoh : ``<nav>Ini Adalah Navbar</nav>``
  - HTML Attributes : properties dari sebuah element HTML
    > Contohnya yaitu : id,class,name | ``<div id="nama">``

## DAY 3 : CSS

### CSS : Cascading Style Sheet
  - CSS dapat digunakan untuk mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya atau lebih tepatnya untuk menstyling sebuah WEB agar terlihat semakin menarik
  - Terdapat 3 cara untuk menambahkan CSS ke dalam dokumen HTML : 
  > - Inline – menggunakan atribut style dalam elemen HTML ``<h1 style="background-color: aqua">Hai.. I'm <span>Dustin</span></h1>``
  > - Internal – menggunakan elemen ``<style>`` di dalam elemen ``<head>``
  ```
  <head>
  <style type="text/css">
    p {color:red; font-size: 15px;}
    .center {display: block; margin: 0 auto;}
    #button-go, #button-back {border: solid 1px black;}
  </style>
</head>
  ```
  > - Eksternal – menggunakan elemen ``<link>`` di dalam elemen ``<head>``, ex ``<link rel="stylesheet" type="text/css" href="style.css">``
### Sintaks Dasar CSS 
  ```
  h1 {
    color: red;
}
  ```
  > - ``Selector`` untuk memilih elemen HTML yang akan kita beri style.

  ```
  properti: "nilai";
  ```
  > - ``Property`` yaitu aturan yang akan diberikan kepada elemen yang dipilih.

  ```
  h1{ 
   background-color: black
} 
  ```
  > - ``Declaration Block`` tempat kita menuliskan atribut atau properti CSS yang akan diberikan ke pada elemen yang telah diseleksi.
  
### Flexbox
  - Flexbox digunakan untuk mengatur jarak antar item pada sebuah container.
  > - ``flex-direction`` : digunakan untuk mengatur arah item didalam container.
  > - ``flex-wrap`` : memungkinkan kita memindahkan item ke baris bawah, apabila baris atas tidak cukup.
  > - ``justyfy-content`` : untuk mengatur rata dari sebuah elemen, seperti rata kiri atau kanan.
  > - ``align-items`` : untuk mengatur kesejajaran item secara vertikal.
  > - ``align-content`` : untuk mengatur jarak antar item terhadap cross-axis.
  > - ``order`` : untuk mengatur urutan dari items.
  > - ``flex-grow`` : untuk mengatur ukuran dari items.
  > - ``align-self`` : untuk mengatur urutan item yang dipilih secara spesifik.

## Day 4 : Algoritma dan Data Struktur | Intro to Javascript

### Algortima
  - Algoritma adalah sederetan langkah-langkah logis yang disusun secara sistematis untuk memecahkan suatu masalah.
  - Manfaat Algoritma
    - Membantu menyederhanakan suatu program yang rumit dan juga besar.
    - Mempermudah pembuatan program yang dapat menyelesaikan masalah tertentu.
  
  - Jenis - jenis Algoritma :
    - **Deskriptif** : Seperti kita menulis tutorial (tata cara) dengan bahasa sehari-hari
    - **Flow Chart** : Metode *Flow Chart* lebih mudah dibaca karena menggunakan gambar visual.
    - **Pseudo Code** :  Penulisan metode ini hampir sama seperti kode pemrograman.
  
  - Contoh Algoritma *Pseudo Code* sederhana menggunakan javascript
  
   ```
  const nama = "Dustin";
console.log("Nama Saya " + nama);
  
  Output : 
  Nama Saya Dustin
  ```
### Javascript 
  > Javacript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website.
  - Syntax dan Statement
     - Syntax bisa dianalogikan seperti kosa kata (vocabulary) dan tata cara (grammar) pada bahasa pemograman.
     - Kita menggunakan syntax tertentu untuk membuat statement program, instruksi untuk djalankan/dieksekusi oleh web browser, compiler, ataupun intrepreter
  - Console log adalah tempat kita untuk cek logic pemograman web yang kita kembangkan.
  - Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming.
    - number 
      > "Tipe data number adalah tipe data yang mengandung semua angka termasuk angka desimal."
    - string 
      > "Tipe data string adalah grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya."
    - boolean 
      > "Tipe data boolean adalah tipe data yang hanya mempunyai 2 buah nilai."
    - null 
      > "Tipe data null adalah tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai."
    - undefined 
      > "Tipe data undefined adalah tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai."
    - object 
      > "Tipe data object adalah koleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya)."
  
### Variable 
  > Variable adalah tempat untuk menyimpan sebuah nilai.
  - Ada 3 cara mendefinisikan sebuah variabel.
    > - var
    > - let
    > - const

