# writting-and-presentation-test# Writing and Presentation Test Week 2

## DAY 1 : Javascript Dasar
### Scope
 - Scope adalah konsep dalam flow data variable.
 - Scope dapat mengatur sampai batas mana suatu variable masih dapat dilihat atau maasih dapat digunakan.
 
 ### Global Scope
  - Variabel global dapat diakses dan dimodifikasi hampir dimana saja di dalam kode program yang kita buat. 
  
  ```
 let namaSaya = "Dustin";

function greeting() {
    return namaSaya;
}

console.log(namaSaya);
  ```
  > Contoh Global Scope
  
 ### Local Scope
  - Variabel yang dideklarasikan dalam local scope hanya bisa di akses dalam scope tersebut dan tidak dapat diakses secara global atau local scope yang lain.
  
  
### Function
 - Function adalah fasilitas untuk membuat suatu program yang dapat kita gunakan berulang ulang tanpa ada batasan selama halaman masih terhubung dengan function tersebut.
 - Kenapa harus membuat function
   - Reusability atau penggunaan kembali dari kode yang sudah kita buat.
   - Untuk menyembunyikan kompleksitas dari prorgram yang kita buat.
   - Dengan adanya function kita dapat dengan mudah mencari letak kesalahan program.
   
 ### Parameter dan Argument
  - Parameter
    - Parameter adalah variabel yang di tulis didalam kurung pada saat function dibuat.
    - Parameter digunakan untuk menampung nilai yang dikirimkan saat function dipanggil
  - Argument
    - Nilai yang dikirimkan ke parameter saat fungsi dipanggil
 ```
 function tambah(a, b) {
  return a + b; // Parameter
}
console.log(tambah(2, 3)); // Argument
 ```
  > Contoh Penggunaan Parameter & Argument
  - Arrow Function
    - Cara lain penulisan dengan menggunakan arrow(panah) "=>" tanpa menggunakan kata kunci "function" dalam syntax.
  ```
let tampilPesan = (nama) => {
  console.log("Halo" + nama);
};
tampilPesan("Dustin");
  ```
  > Contoh Penggunaan Arrow Function
  
## DAY 2 : Data Type Built in Prototype & Method
### Tipe Data
  > Tipe data yaitu berfungsi untuk membedakan tipe nilai satu dengan yang lainnya.
###
    
  - String : Berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks.
 ```
const x = "Ini adalah string";
const y = "Ini adalah string dengan kutip tunggal";
 ```
 
 ```
 // membuat method baru utk tipe data string ( Prototype )
String.prototype.reverse = function(){
  let a = ""
  for (let i = String(this).length-1; i >= 0 ; i--) {
    a = a + String(this)[i]
  }

  return a
}

// method yg dimiliki oleh string
console.log("Yassap".reverse())
console.log("Saya Dustin".reverse())

// function dgn argumen string
// console.log(reverse("hallo"));
 ```
 
  - Number : Tipe Data Numbers adalah tipe data numerik yang menampung bilangan bulat.
```
let angka = 3.12345
console.log(angka.toFixed(1)) // 3.1
console.log(angka.toFixed(2)) // 3.12
```

  - Math : Adalah objek bawaan yang memiliki properti dan metode untuk konstanta dan fungsi matematika.
```
// properties
console.log(Math.PI)

// method
console.log(Math.abs(-5)) // 5
console.log(Math.ceil(5.2)) // 6
console.log(Math.floor(5.6)) // 5
console.log(Math.round(5.6)) // 6
console.log(Math.round(5.2)) // 5
console.log(Math.random()) 
```

### Primitif & Non Primitif
  - Tipe Data Primitif
    - String
    - Number
    - BigInt
    - Boolean
    - undefined
    - null
    - Symbol
  - Tipe Data Non Primitif
    - Object
    - Array



## DAY 3 : DOM - Introduction.
  - Document Object Model atau DOM adalah Interface pemrograman untuk memanipulasi dokumen HTML, DOM mewakili dokumen HTML sebagai Tree atau Pohon, DOM menyediakan fungsi yang memungkinkan kita untuk menambah, menghapus dan memodifikasi bagian Dokumen secara efektif.
### Selecting Element.
   - Mengakses DOM.
     - ``let document.getElementById()`` : Berdasarkan *Id*
     - ``let document.getElementByName()`` : Berdasarkan *Name*
     - ``let document.getElementsByClassName()`` : Berdasarkan *Class*
     - ``let document.getElementsByTagName()`` : Berdasarkan *Tag Name*
     - ``let document.querySelector()`` : Berdasarkan *CSS Selector*
     
### Traversing Element.
  - ``let x = node.parentNode`` : Untuk mengambil *Parent* dari suatu Element
  - ``let x = parentElement.firstChild`` : Untukk mengambil *Child* dari suatu Element
  - ``let x = currentNode.nextElementSibling`` : Untuk mengambil *Siblings* dari suatu Element
  
## DAY 4 : DOM - Manipulating 
### Manipulating Element.
```
let app = document.getElementById("app")
```
```
app.innerHTML = "<h1>Hai</h1>
```
  > Memberikan Konten.
  
```
let p = document.createElement("p")
p.innerText = "ini adalah paragraf"
```
  > Membuat Element.
 ```
 app.append(p)
 
 let p2 = document.createElement("p")
 p2.innerText = "paragraf ke-2"
 app.appendChild(p2)
 ```
   > Menambahkan child kedalam parent.
 
 ```
 let end = document.getElementById("end")
 end.remove()
 ```
   > Remove Element.
 
### Manipulating Style.
 ```
 let testing = document.getElementById("testing")
 let testingStyle = getComputedStyle(testing)
 console.log(testingStyle.height)
 ```
   > Mengambil style dari Element.
   
## DAY 5 : Event & Form.
### Event
  - Event adalah aktifitas yang terjadi pada halaman website.
  - Cara Membuat Event pada Paragraf.
```
let paragraf = document.getElementById("paragraf");

paragraf.onclick = function () {
  alert("ini dari paragraf");
};
```
  - Membuat Event pada Button.
```
let button = document.getElementById("btn");
button.addEventListener("click", function () {
  alert("ini button");
});
```
  - Membuat Confirm Event .
```
button.addEventListener("click", function () {
  confirm("ini adalah button?");
});
```
### Form.
```
let loginForm = document.querySelector("#login-form");
let inputUsername = document.querySelector("#username");
let inputPassword = document.querySelector("#password");

// Mengambil value dari form.
loginForm.addEventListener("submit", (event) => {
  event.preventDefault();
  console.log(inputUsername.value);
  console.log(inputPassword.value);

```
  > Nilai akan diambil dari hasil input form.
  - Menampilkan hasil dari value.
```
let userLogin = {
    username: inputUsername.value,
    password: inputPassword.value,
  };

  console.log(userLogin);
  ```
  > Nilai yang berhasil diambil akan ditampilkan di console.
    - Mengecek apakah nilai ada atau tidak.
 ```
   if (userLogin.username == user.username && userLogin.password == user.password) {
    console.log("login berhasil");
  } else {
    console.log("user tidak ditemukan");
  }
});
 ```
   > Jika nilai tidak ada, maka hasil outputnya user tidak ditemukan.
 ```
 loginForm.reset();
 ```
   > Berguna untuk mereset form setelah nilai diinput.
