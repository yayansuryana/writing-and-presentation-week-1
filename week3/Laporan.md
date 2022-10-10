## **Javascript Intermediate**

### **Array dan Multidimensional Array**
- **Array** adalah sebuah tipe data non-primitif yang mampu menyimpan banyak data serta mampu menyimpan berbagai macam tipe data. Cara menggunakan array adalah dengan menggunakan kurung kotak, seperti let arr [ ]. Contoh dari array sebagai berikut :
```
let arr = ["Hallo", 1, true];
Atau bisa juga

let bunga = ['Melati',  'Tulip', 'Anggrek'];
console.log(bunga);
```
- Cara mengakses array, Array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0. Contoh syntax :
```
let buku = ["Buku Cerita", "Buku Pelajaran", "Buku Dongeng"];
console.log(buku);

Output :
Array(3)
0 : "Buku Cerita"
1 : "Buku Pelajaran"
2 : "Buku Dongeng"

Array sepanjang 3 serta terdapat 2 index dalam array.
```
- **Update Array** , cara mengupdate array yaitu :
```
let buku = ["Buku Cerita", "Buku Pelajaran", "Buku Dongeng"];

buku[0] = "Buku Sejarah";
console.log(buku);

Output : ["Buku Sejarah", "Buku Pelajaran", "Buku Dongeng"]
```
- **Const in array**, Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain. tetapi const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable). Contoh syntax :
```
const warna = ['Merah', 'Putih', 'Biru'];
warna[1] = ['Kuning'];
 
console.log(warna);
Output : ['Merah', 'Kuning', 'Biru'];
```
- **Array Properti**, Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.Array properti terdiri dari :
  - **.length**, length akan mengembalikan nilai dari jumlah panjang data suatu array. Contoh syntax :
    ```
    let arr = ["Hallo", 1, true]
    console.log(arr.length);
    
    Output : 3
    ```
  - **.constructor**, constructor mengembalikan referensi ke fungsi array yang membuat objek.
  - **.prototype**, prototype mewarisi definisi array dengan menambah properti dan metode.
  - **.index**, mewakili indeks kecocokan berbasis nol dalam string.
  - **.input**, properti ini hanya ada dalam array yang dibuat oleh kecocokan ekspresi reguler.
- **Array Methods**, Array memiliki method atau biasa disebut built-in methods. Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.
 - **.push()** adalah method yang digunakan untuk menambah data diakhir. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   console.log(arrBuah);
   
   arrBuah.push("Duku")
   console.log(arrBuah); //Output : "Jeruk", "Pepaya", "Rambutan", "Duku"
   ```
 - **.unshift()** adalah method yang digunakan untuk menambahkan data didepan. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.unshift("Mangga")
   console.log(arrBuah); //Output : "Mangga", "Jeruk", "Pepaya", "Rambutan"
   ```
 - **.pop()** adalah method yang digunakan untuk menghapus elemen terakhir. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.pop()
   console.log(arrBuah); //Output : "Jeruk", "Pepaya"
   ```
 - **.shift()** adalah method yang digunakan untuk menghapus elemen depan. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.shift()
   console.log(arrBuah); //Output : "Pepaya", "Rambutan"
   ```
 - **.splice()** adalah method yang digunakan untuk menghapus ditengah. Dalam slice terdapat start atau awal/index, deletecount atau banyak data yang didelete, dan item atau data yang disisipkan. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan",
   "Anggur",
   "Semangka"
   ];
   arrBuah.splice(2) 
   console.log(arraBuah); //Output : "Jeruk", "Pepaya"
   
   arrBuah.splice(2, 1)
   console.log(arrBuah); //Output : "Jeruk", "Rambutan", "Anggur", "Semangka"
  
   arrBuah.splice(2, 1, "Buah Naga")
   console .log(arrBuah); //Output : "Jeruk", "Buah Naga", "Rambutan", "Anggur", "Semangka"
   ```
 - **.slice()** digunakan untuk mengembalikan shallow to copy (copy data) atau mengambil data dengan cara copy data. Contoh script :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan",
   "Anggur",
   "Semangka"
   ];
   let slice = arrBuah.slice(2, 4)
   console.log(slice); //Output: "Pepaya", "Anggur"
   
   let slice = arrBuah.slice(2)
   console.log(slice); //Output : "Rambutan", "Anggur", "Semangka"
   ```
- **Looping Array**, Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach(). Contoh script looping :
   ```
   let arrBuah = ["Anggur", "Jeruk", "Semangka", "Pepaya", "Rambutan", "Duku"];
   for(let i = 0; i<arrBuah.length; i++){
   console.log(arrBuah[i])
   };
   //Output : 
   Anggur
   Jeruk
   Semangka
   Pepaya
   Rambutan
   Duku
  
   Atau bisa juga
   for(let i = arrBuah.lengthh-1; i>0; i--){
   console.log(arrBuah[i])
   };
   //Output :
   Duku
   Rambutan
   Pepaya
   Semangka
   Jeruk
   Anggur
   ```
 - **.forEach()** adalah method untuk melakukan looping pada setiap elemen array. ForEach ini tanpa menggunakan return.Contoh script :
   ```
   arrBuah.forEach((item) => {
    console.log(item)
   });
   //Output :
   Anggur
   Jeruk
   Semangka
   Pepaya
   Rambutan
   Duku
  
   Contoh lain
   arrBuah.forEach((index,item) =>{
   if(index %2 == 1){
    console.log(index,item)
   }
   });
   //Output :
   1. Jeruk
   3. Pepaya
   5. Duku
   Script diatas digunakan untuk menampilkan index array ganjil.
   ```
 - **.map()** melakukan perulangan/looping dengan membuat array baru.Contoh script :
   ```
   let buah segar = arrBuah.map((item) =>{
   return item + " " + "segar"
   });
   //Output :
   0 : Anggur segar
   1 : Jeruk segar
   2 : Semangka
   3 : Pepaya
   4 : Rambutan
   5 : Duku
   ```
- **Array Multidimensional** Multidimensional Array bisa dianalogikan dengan array of array. Ada array didalam array. Contoh script :
   ```
   let arrMulti = [
   ["nama", "alpha"],
   ["umur", 17],
   ["kelas",  "JS"],
   ]
   console.log(arrMulti[0][1];
   //Output : "alpha"
   
   Atau bisa juga
   arrMulti[2][1] = "CSS"
   console.log(arrrMulti);
   Script diatas berarti teks JS dirubah menjadi CSS
   ```
   
   ### **Javascript Object**
- **Object** adalah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object.
- **Membuat sebuah object** Sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel. Contoh script :
   ```
   let siswa = {
    nama : 'terra',
    umur : 17,
    hobi : 'memancing', 
    "nomor handphone" : 08256814086
    }
    console.log(siswa);
    ```
- **Cara akses object** Dalam mengakses object terdapat 2 cara yaitu menggunakan dot notation dan bracket. Selain itu, bisanya dalam mengakses object yaitu menggunakan console.log(object).
  - dot notation, misalnya ``console.log(siswa.nama);`` maka output yang dihasilkan yaitu terra
  - bracket, misalnya ``console.log(siswa['nama']);`` 
- **Memanggil nama object dengan variable** contohnya :
    ```
    let properti = "umur"
    console.log(siswa[properti]);
    ```
- **Menambahkan properti baru ke dalam object** Contoh script:
    ```
    Cara 1
    let buku = {
     Judul : "Mantan jadi manten",
     Penulis : "Hayati",
     "Jumlah halaman" : 250,
     };
     buku.tahun : 2022;
     buku.terjual : 3000;
     console.log(bukuu);
     //Output :
     Judul : Mantan jadi manten
     Penulis : Hayati
     Jumlah halaman : 250
     buku.tahun : 2022
     buku.terjual : 3000
     
     Cara 2
     buku["penerbit"] : "gramedia";
     console.log(buku);
     //Output :
     Judul : Mantan jadi manten
     Penulis : Hayati
     Jumlah halaman : 250
     buku.tahun : 2022
     buku.terjual : 3000
     penerbit : gramedia
     ```
- **Ganti properti lama** contoh script : 
     ```
     Cara 1
     let hewan = {
      nama : 'kucing',
      kaki : 4,
      warna : 'putih',
     };
     hewan.nama : 'kelinci',
     hewan.warna : 'hitam',
     console.log(hewan);
     //Output 
     nama : kelinci
     kaki : 4
     warna : hitam
     
     Cara 2
     hewan["kaki"]=2;
     console.log(hewan)
     nama : kelinci
     kaki : 2
     warna : hitam
     ```
- **Delete Properti** contoh script :
     ```
      let hewan = {
      nama : 'kucing',
      kaki : 4,
      warna : 'putih',
     };
     delete.hewan.warna;
     delete.hewan.kaki;
     console.log(hewan);
     //Output : nama : kucing
     ```
- **Method** adalah ketika ingin menambahkan sebuah function. Ada 2 method dalam object, yaitu :
  - **const greeting** contoh script :
    ```
    const greeting = {
     welcome : function(){
      return "halo selamat datang";
    };
     afterpay:function(){
     return "terimakasih sudah membeli produk kami";
     }
    };
    console.log(greeting.welcome()); //Output : halo selamat datang
    ```
  - **nested object** contoh script :
    ```
    let buku = {
     Judul : "Tips jago Javascript",
     Tahun : 2022;
     Penulis {
        Penulis1 : {
           Nama : "Suryana",
           Umur : 20,
           Kota : "Bandung"
           }
        Penulis2 : {
           Nama : "Yayan",
           Umur : 22,
           Kota : "Cilacap"
           }
        Penulis3 : {
           Nama : "Nuri",
           Umur : 20,
           Kota : "purwokerto"
           }
         }
    };
     console.log(buku.penulis.penulis1.nama);//Output : Suryana
    ```
- **Built In Method (Object menjadi array** 
     ```
     let siswa = {
       nama : "Yayan",
       umur : 22,
       hobi : "Bermain game",
     };
     console.log(object.keys.(siswa)); //Output : 'nama', 'umur', 'hobi'
     console.log(object.values.(siswa)); //Output : 'Yayan', '22', 'Bermain game'
     ```
- **Looping Object** Looping sendiri berarti perulangan. Jika kita ingin menampilkan seluruh object properti, kita bisa menggunakan looping. Jadi tidak perlu mengakses secara manual memanggil setiap propertinya. Contoh scriptnya :
    ```
    let siswa = {
     nama : "Yayan",
     umur : 22,
     kota : "Jakarta",
    };
    for(let key in siswa){
      console.log(siswa[key]); 
    //Output :
    Yayan
    22
    Jakarta
    ```
- **Array of Object** adalah array yang menyimpan banyak object sebagai nilainya. Contoh script :
    ```
    let users = {
      {
       Nama : "Reyhan",
       Umur : 28,
       Kota : "Jakarta",
      },
      {
       Nama : "Yayan",
       Umur : 20,
       Kota : "Bandung",
      },
      {
       Nama : "Suryana,
       Umur : 24,
       Kota : "Cilacap",
      },
    };
    console.log(user);
    
    Dengan menggunakan Map, maka
    let data = users.map((el) => {
     console.log(el.nama);
    });
    //Output :
    Reyhan
    Yayan
    Suryana
    ```
    
    ### **Rekrusif dan Modules**
- **Rekrusif** adalah function atau algoritma yang memanggil dirinya sendiri sampai kondisi tertentu. Rekrusif ini mirip seperti looping. Misalnya pada gambar ada gambar di dalam gambar. Rekrusif dapat diartikan sebagai teknik pemrograman yang menggunakan function atau fungsi. Sederhananya adalah fungsi yang memanggil fungsi tersebut atau dirinya sendiri, seolah-olah terjadi suatu perulangan. Proses pemanggilan inilah yang disebut sebagai recursion (rekursi) dan akan terus dilakukan sampai pada kondisi yang sudah ditentukan. Terdapat 2 kunci pada rekrusif, yaitu Base Case/titik berhenti adalah kasus dasar untuk menyelesaikan permasalahan. Base case akan dikunjungi jika rekursi berakhir (kondisi untuk berhenti terpenuhi), serta mengembalikan nilai tanpa melakukan rekursi kembali. dan Recrusion Case/titik memanggil function yaitu permasalahan yang ada tentunya akan diperkecil dengan melakukan pemanggilan function itu sendiri (recursion call). Permasalahan dapat diperkecil dengan mengurangi atau memecahkan data input pada setiap pemanggilannya hingga mencapai base case. Contoh script:
  ```
  Menampilkan bilangan 1 2 3 4 5
  
  function deretAngka(n){
   if (n == 1) { //base case
     console.log(n)
   } else { //recrusion case
     deretAngka(n-1)
     console.log(n);
    }
  }
  deretAngka(3)
  
  Atau contoh lain :
  Mencari angka faktorial
  Misalnya 5!
  Solusinya jika dijabarkan 5 x 4 x 3 x 2 x 1

  function faktorial(n) {
    if (n == 1) {
      return 1
    } else {
      return n * faktorial(n - 1)
    }
  }
  console.log(faktorial(3))
  //Output = 6
  ```
- **Modules** adalah cara untuk memisahkan kode ke file yang berbeda. Keuntungan dari modules yaitu mudah untuk mengelola kode serta kode tidak menumpuk di dalam satu file. Terdapat 2 kata kunci pada modules yaitu export dan import. Modules juga dapat diartikan sebagai sebuah cara bagi JavaScript untuk mengisolasi kode dari suatu file ke dalam sebuah file terpisah. Sehingga kode tersebut dapat digunakan berulang kali dengan cara di-export dari suatu file dan di-import ke file yang lainnya. Kita dapat melakukan export kode apapun pada JavaScript seperti string, object, array, number, hingga function.
- **Export**, digunakan untuk meng-export variabel pada file JavaScript. Variabel yang di_export_ dapat berisi data seperti string, object, array, hingga function. Hal ini dilakukan agar file JavaScript tersebut dapat dijadikan sebuah module, sehingga variabel yang telah di-export dapat digunakan pada file JavaScript lain dengan menggunakan import. Contoh script :
  ```
  // File Jepang.js
  export let motor = ["suzuki", "yamaha", "honda", "kawasaki"]
  
  let entertainment = ["anime", "manga", "wibu", "dorama"]
  export default entertainment
  
  export function sayHello() {
   console.log("hallooo")
  }
  
   // File Amerika.js
  let apple = ["iphone", "macbook", "imac"]
    export {apple}
  ```
- **Import**, diibaratkan sebagai pasangan dari export. Jadi import digunakan untuk menggunakan variabel yang sudah di-export dari module lainnya. Contoh script :
  ```
  import {apple} from './amerika.js';
   console.log(apple);
  
  // File Indonesia.js
  import {motor} from "./Jepang.js"
   console.log(motor);
   
  import Entertainment, { motor as motorJepang, sayHello  } from "./jepang.js"
  console.log(Entertainment);
  ```
- Berdasarkan contoh script diatas, maka : 
  - Indonesia hanya bisa import, karena dia file utama.
  - Jepang bisa melakukan import dan export.
  - Amerika hanya melakukan export.
- Hal hal yang harus dilakukan saat membuat modules adalah menambahkan type="module" pada script utama, lalu siapkan script ke-2 dan sebagainya untuk melakukan export, serta lakukan import pada file atau script utama.

### **Asynchronous dan Synchronous**
- **Synchronous** seperti saat kita mengeksekusi perintah satu persatu dan berurutan. Dalam hal ini, ia hanya dapat mengeksekusi satu perintah pada satu waktu dan harus menunggu satu perintah tersebut selesai sebelum melanjutkan perintah selanjutnya. Contoh script :
```
console.log("antrian 1");
console.log("antrian 2");
console.log("antrian 3");

// output
// antrian 1
// antrian 2
// antrian 3
```
- **Asynchronous** berarti mengizinkan komputer untuk memproses perintah lain sambil menunggu suatu proses lain yang sedang berlangsung. Ini artinya kita bisa melakukan lebih dari 1 proses sekaligus (multi-thread). 2 cara untuk membuat proses asynchronous yaitu :
 - **setTimeout(function, milliseconds)** digunakan untuk simulasi pemanggilan kembali proses asynchronous yang sedang/sudah selesai dijalankan. Pemanggilan hanya dilakukan 1 kali. Contoh script :
   ```
   setTimeout(() => {
   console.log("Cuci baju"); // proses asynchronous
   }, 1000);
   console.log("Menyapu");
   console.log("Mengepel");
   console.log("Memasak");

   // 1000 ms = 1 second

   // Output:
   // Menyapu
   // Mengepel
   // Memasak
   // Cuci baju
   ```
 - **setInterval(function, milliseconds)** digunakan untuk simulasi pemanggilan proses asynchronous yang sedang/sudah dijalankan dalam interval waktu tertentu. Pemanggilan dilakukan berkali-kali sesuai interval waktu yang ditentukan. Contoh script :
   ```
   setInterval(() => {
   console.log("Cuci baju"); // proses asynchronous
   }, 3000);
   console.log("Menyapu");
   console.log("Mengepel");
   console.log("Memasak");

   // 3000 ms = 3 second

   // Output:
   // Menyapu
   // Mengepel
   // Memasak
   // Cuci baju (x time)

   // Cuci baju akan dijalankan setiap 3 detik sekali
   ```
- Terdapat beberapa cara dalam membuat asynchronous secara simulasi artinya tidak murni asynchronous, antara lain :
  - **Callback** adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya. Contoh script :
    ```
    function proses1() {
    console.log("proses 1 selesai dijalankan");
    }

    function proses2(callback) {
    setTimeout(function () {
     console.log("proses 2 selesai dijalankan");
     callback();
     }, 100);
    }

    function proses3() {
    console.log("proses 3 selesai dijalankan");
    }
    proses1();
    proses2(proses3);

    Output
    proses1 selesai dijalankan
    proses2 selesai dijalankan
    proses3 selesai dijalankan
    
    Dalam hal ini apabila proses2 membutuhkan waktu saat diproses, maka proses3 dijalankan terlebih dahulu. Lalu apabila proses2 selesai diproses maka akan dicallback untuk menampilkan hasil console.lognya.
    ```
  - **Promise** adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API. Promise sesuai dengan artinya adalah janji. Seperti ketika kita berjanji, jika apa yang kita janjikan bisa kita lakukan maka kita harus melakukannya, jika janjinya ada halangan maka kita tidak bisa melakukannya atau jika janji tersebut belum pada waktunya kita juga harus menunggunya. Dalam pengambilan data, promise memiliki 3 kemungkinan state yaitu Pending(sedang dalam proses), Fulfilled (berhasil), serta Rejected (gagal). Contoh script:
    ```
    const condition = true;

    let newPromise = new Promise((resolve, reject) => {
    if (condition) {
    // apa yang dilakukan jika promise 'fulfilled'
    resolve("Berhasil");
    } else {
    // apa yang dilakukan jika promise 'rejected'
    reject(new Error("Error Gagal"));
    }
    });

    newPromise
    .then((result) => {
    console.log(result); // Output: Berhasil
    })
    .catch((error) => {
    console.log(error);
    })
    .finally(() => {
    console.log(
      "Finally tetap terpanggil dalam kondisi fulfilled ataupun rejected"
    ); // Output: Finally tetap terpanggil dalam kondisi fulfilled ataupun rejected
    });
    ```
  - **Async-await** adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise. Async berfungsi untuk mengubah function synchronous menjadi asynchronous. Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil. Contoh script :
    ```
    // Definisikan dahulu promise yang ingin digunakan
     let condition = true;
     let tesAsyncAwait = async (condition) => {
     if (condition) {
      return "Condition is fulfilled!";
     } else {
      throw "Condition is rejected!";
       }
     };

     // Membuat fungsi run menjadi asynchronous menggunakan async/await
     const run = async (condition) => {
      try {
     const message = await tesAsyncAwait(condition);
     console.log(message);  // Output: Condition is fulfilled!
     console.log("After condition is fulfilled"); // Output: After condition is fulfilled
     } catch (error) {
     console.log(error);
      }
     };

     run(true);
     ```
     
### **Web Storage**
- **Web Storage** adalah tempat menyimpan suatu data. Berbeda dengan objek atau array, data yang disimpan pada objek atau array JavaScript bersifat sementara, dan akan hilang jika terjadi reload atau pergantian URL pada browser. Sedangkan data yang disimpan pada Web Storage akan bertahan lebih lama karena data akan disimpan pada storage browser. Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage. Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer oleh web browser saat menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB). Penyimpanan data pada local storage dan session storagelebih besar yaitu 5MB per page tanpa mempengaruhi kinerja situs web. Namun, penting untuk diketahui agar tidak menyimpan data sensitif seperti password ke dalam local storage ataupun session storage untuk menghindari serangan pencurian data. Hal yang harus diperhatikan dalam web storage yaitu preferensi user, setting, score, serta posisi video. Dan dalam web storage terdapat study case yaitu fitur dark mode, detail page, serta todo. Hal-hal yang dilakukan dalam membuat light-dark mode yaitu atur tema light dengan css, buat function handle darkmode dengan javascript, lalu buat tombol button diklik handle dark-mode dengan html. Contoh script :
  ```
  //File HTML
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta http-equiv="X-UA-Compatible" content="IE=edge" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Todo List</title>
      <link rel="stylesheet" href="style.css" />
    </head>
    <body class="">
      <form action="" class="container">
        <input type="text" placeholder="Hari ini saya akan..." />
        <ul id="list-container"></ul>
      </form>
      <button id="toggle">Toggle</button>

      <script src="script.js"></script>
    </body>
  </html>
  ```
  ```
  //File CSS
  @import "https://fonts.googleapis.com/css?family=Poppins";

  /*
    hint untuk dark-theme
    :root 
    var()  
    bisa cek folder dark-mode
  */

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    background: #e0e0e0;
    min-height: 100vh;
    font-family: "Poppins", Arial, Helvetica, sans-serif;
  }

  body.dark {
    background: black;
    color: white;
  }

  .container {
    padding-top: 50px;
    max-width: 500px;
    margin: auto;
  }

  input {
    width: 100%;
    padding: 5px 8px;
    border: 1px solid rgb(121, 121, 121);
    border-radius: 8px;
  }

  #list-container li {
    margin: 10px 0;
    padding: 8px 12px;
    list-style: none;
    background: #e0e0e0;
    border: 1px solid rgb(180, 180, 180);
    border-radius: 8px;
    box-shadow: 23px 23px 46px #d0d0d0, -23px -23px 46px #f0f0f0;
  }
  ```
  ```
  //File Javascript Theme
  // ==================== check ketika pertama kali website di buka, apakah ada key: theme dan value: dark di storage
  if (localStorage.getItem("theme") === "dark") {
    document.body.classList.add("dark");
  } else {
    document.body.classList.remove("dark");
  }

  // ==================== check ketika pertama kali website di buka, apakah ada key: theme dan value: dark di storage
  document.getElementById("toggle").onclick = () => {
    if (localStorage.getItem("theme")) {
      localStorage.removeItem("theme");
      document.body.classList.remove("dark");
    } else {
      localStorage.setItem("theme", "dark");
      document.body.classList.add("dark");
    }
  };
  ```
  ```
  //File Javascript todo
  // ==================== init penampung list dari todo
  const todos = [];

  // ==================== check ketika pertama kali website di buka, apakah ada key: theme dan value: dark di storage
  if (localStorage.getItem("todo")) {
    const todoStore = JSON.parse(localStorage.getItem("todo"));

    todoStore.map((todo) => {
      const li = document.createElement("li");
      li.innerText = todo;

      const container = document.querySelector("#list-container");
      return container.appendChild(li);
    });
  }

  // ==================== check ketika pertama kali website di buka, apakah ada key: theme dan value: dark di storage
  document.querySelector("form").addEventListener("submit", (ev) => {
    ev.preventDefault();
    const userInput = document.querySelector("input").value;

    const li = document.createElement("li");
    li.innerText = userInput;

    todos.push(userInput);

    localStorage.setItem("todo", JSON.stringify(todos));

    const container = document.querySelector("#list-container");
    container.appendChild(li);
  });

  /* 
    Conclucion:
    JSON.parse -> ubah string ke object 
    JSON.stringify -> ubah apapun ke string JSON
  */
  ```
