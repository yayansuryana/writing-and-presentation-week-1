# Writing and Presentation Test Week 2

## **Javascript Scope dan Function**

### **Javascript Scope**
- **Scope** adalah Scope adalah konsep dalam flow data variabel. 
- **Blocks** adalah code yang berada didalam curly braces {}.
- **Global scope** adalah variabel yang dibuat dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks. Contoh script :
  ```
  let myName = 'Yayan';
  
  function greeting() {
    return myName;
  }
  console.log(myName);
  ```
- **Local scope** adalah mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping. Maka variabel hanya bisa diakses didalam blocks saja. tidak bisa diakses diluar blocks. Contoh script :
  ```
  function greeting(){
      let MyName = 'Suryana'
      return myName
  }
  
  console.log(greeting())
  greeting(myName)
  ```
  
### **Javascript Function**
- **Function** adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur. Contoh script :
  ```
  function greeting() {
      return 'Hello world!';
  };
  
  Penjelasan script
  - function adalah function keyword.
  - greeting adalah identifier.
  - { return 'Hello World!' } adalah function body
  ```
- Perbedaan console.log() dan return adalah console.log() hanya menampilkan informasi ke dalam tab console JavaScript, sedangkan return akan mengembalikan sebuah nilai ke tempat di mana fungsi itu dipanggil.
- **Cara memanggil function**
  ```
  greeting()
  console.log(greeting());
  
  Dalam hal ini fungsi greeting() return valuenya adalah 'Hello world!'. Nilai dari return ini akan dikembalikan ke tempat pemanggilan fungsi tersebut, sehingga kode di atas saat dijalankan sebenarnya akan menjadi console.log('Hello world!)
  ```
- **Parameter Function** dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas. Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function pengurangan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.  Contoh script :
  ```
  function pengurangan(a, b) {
      return a - b;
  }
  ```
- **Argumen Function** adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah parameternya, jadi jika di function pengurangan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen. Contoh script :
  ```
  function pengurangan(a, b) {
      return a - b;
  }
  console.log(pengurangan(10, 5)) //output: 5
- **Default Parameter** digunakan untuk memberikan nilai awal atau default pada parameter function. Default parameters bisa digunakan jika ingin menjaga function agar tidak error saat dipanggil tanpa argumen. Contoh script :
  ```
  function salam(nama = 'orang'){
        return 'Haii' + nama
    }
    
    console.log(salam('Diana'))
    console.log(salam())
    ```
- **Function Helper** Kita bisa menggunakan function yang sudah dibuat pada function lain. Contoh script :
    ```
    function multiplyByNineFifths(number) {
      return number * (9/5);
    };
    function getFahrenheit(celcius) {
      return multiplyByNineFifths(celcius) + 32;
    };
    getFahrenheit(15); //returns 59
    ```
- **Arrow Function** adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version). Contoh script :
    ```
    const greeting = () => {
      return 'Hello wordl!';
    };
    
    const pengurangan = (a, b) => {
      return a - b;
    };
    ```
- **Short Syntax Function**
  - Zero Parameter
    ```
    const functionName = () => {};
    ```
  - One Parameter
    ```
    const functionName = paramOne => {};
    ```
  - Two or More Parameter 
    ```
    const functionName = (paramOne, paramTwo) => {};
    ```
  - Single-line block 
    ```
    const sumNumbers = number => number + number; 
    ```
  - Multi-line block 
    ```
    const sumNumbers = number => {
      const sum = number + number ;
      return sum;
    };
    ```
### **Eror dan Debbuging**
- Error objek dilempar ketika kesalahan runtime terjadi. Objek Errorjuga dapat digunakan sebagai objek dasar untuk pengecualian yang ditentukan pengguna. Kesalahan runtime menghasilkan Errorobjek baru yang dibuat dan dibuang.
- Tipe-tipe pada eror antara lain :
  - **EvalError**, yaitu membuat instance yang mewakili kesalahan yang terjadi terkait fungsi global eval().
  - **RangeError**,yaitu membuat instance yang mewakili kesalahan yang terjadi saat variabel numerik atau parameter berada di luar rentang validnya.
  - **ReferenceError**,yaitu membuat instance yang mewakili kesalahan yang terjadi saat mereferensikan referensi yang tidak valid.
  - **SyntaxError**, yaitu membuat instance yang mewakili kesalahan sintaks.
  - **TypeError**, membuat instance yang mewakili kesalahan yang terjadi saat variabel atau parameter bukan tipe yang valid.
  - **URIError**, membuat instance yang mewakili kesalahan yang terjadi saat encodeURI()atau decodeURI()melewati parameter yang tidak valid.
  - **AggregateError**, membuat instance yang mewakili beberapa kesalahan yang dibungkus dalam satu kesalahan ketika beberapa kesalahan perlu dilaporkan oleh suatu operasi, misalnya oleh Promise.any().
  - **InternalError**, membuat instance yang mewakili kesalahan yang terjadi saat kesalahan internal di mesin JavaScript dilemparkan. Misalnya "terlalu banyak rekursi".
  - **Constructor**, yaitu membuat error objek baru.
  - **Metode Statis** terdiri dari Error.captureStackTrace(), Error.stackTraceLimit, Error.prepareStackTrace()
  - **Instance Properties** terdiri dari Error.prototype.message, Error.prototype.name, Error.prototype.cause
- Debugging pada Javascript yang paling umum adalah dengan console.log() variabel yang ingin diperiksa. Terdapat 2 cara dalam debugging, yaitu :
  - Menggunakan alat pengembang chrome, buka halaman dengan kode JS (tekan cmd+o di macOS atau Ctrl+o di Windows) dan pilih file untuk di-debug, klik baris yang ingin didebug dan segarkan kembali halaman (F5).
  - Call Stack, jalur yang telah diambil program untuk mencapai titik saat menetapkan titik putus atau mengalami kesalahan. Contoh script :
    ```
    (function testing(){
        var obj = {
        add
    }
    function add(a, b) {
        var result = a + b
        return result.split('')
    }
    var stringResult = obj.add("1", "2") // stringResult becomes "12"
    var numberResult = obj.add(1, 2) // numberResult is never set, an error is thrown
    })()
    
    Penjelasan :
    - testing dipanggil secara otomatis karena ini adalah IIFE (immediately Invoked Function Expression);
    - variabel obj dideklarasikan dengan function add (menggunakan ES6 shorthand untuk fungsi dalam objek, itu akan sama dengan memiliki var obj = { add: add };
    - function add dipanggil dari variabel obj dengan dua string memiliki parameter, ada yang ditambahkan yang menjadikannya "12" dalam skenario ini dan kemudian split dipanggil sebelum mengembalikan ["1", "2"];
    - function add dipanggil lagi, kali ini dengan angka, nilai ditambahkan sehingga menjadi 3 tetapi kemudian, split (yang tidak tersedia untuk variabel tipe angka ) dipanggil yang membuat error dilemparkan;
    ```
- Alat untuk menghindari runtime errors antara lain :
  - Quokka untuk mengevaluasi kode pada saat mengetik.
  - Eslint untuk memastikan panduan gaya konsisten dan itu akan membawa satu atau dua kesalahan di sepanjang mengoding.
  - Untuk yang ingin menjadikan JS pengalaman mengetik yang lebih kuat, maka dapat melihat hal-hal seperti TypeScript.

## **Data Type Built in Prototype & Method**

- Data Type

Data types atau tipe data adalah sebuah pengklasifikasian data berdasarkan jenis data tersebut. Tipe data dibutuhkan agar kompiler dapat mengetahui bagaimana sebuah data akan digunakan.

- String

string adalah tipe data untuk teks yang terdiri dari gabungan huruf, angka, dan berbagai karakter. Fungsi ini digunakan untuk membuat identifier string atau teks.

- Number

Tipe Data Numbers (Numerik) Tipe data integer adalah tipe data numerik yang menampung bilangan bulat. Contohnya bilangan 1,2,3 dan seterusnya

- Math

Math adalah objek bawaan yang memiliki properti dan metode untuk konstanta dan fungsi matematika. Ini bukan objek fungsi, Tidak seperti banyak objek global lainnya, Math bukanlah sebuah konstruktor. Semua properti dan metode Math bersifat statis. Anda merujuk ke pi konstan sebagai Math.PI dan Anda memanggil fungsi sinus sebagai Math.sin(x), di mana x adalah argumen metode. Konstanta didefinisikan dengan presisi penuh bilangan real dalam JavaScript.

- Primitive dan non Primitive

Tipe data primitif itu hanya punya value tidak punya properti atau method. Contoh tipe data ini : number, boolean,null, string,integer,long, double. Non primitif artinya tidak didefinisikan secara default harus diisi sendiri seperti array dan class dimana didalamnya terdapat string,int, dll.
Perbedaan utama antara tipe data primitif dan non-primitif adalah: Jenis primitif sudah ditentukan sebelumnya (sudah ditentukan) di Java. Tipe non-primitif dibuat oleh programmer dan tidak ditentukan oleh Java (kecuali untuk String ).

Primitive

 - Numbers
 - Strings
 - Booleans
 - undefined
 - null

Non primitive

 - Objects
 - Arrays
 - Functions
