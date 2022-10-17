# **Writing Minggu ke-4**

## **Javascript-Asynchronous**

### **Async-Await**
- **Async Await** adalah Async await adalah salah satu fitur baru dari Javascript yang digunakan untuk menangani hasil dari sebuah Promise. Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil. Async await juga dapat diartikan sebagai cara untuk menangkap suatu objek tertentu. Contoh scriptnya yaitu :
```
let nonton = (kondisi) => {
    return new Promise((resolve, reject) => {
    if (kondisi == "jalan") {
        resolve("nonton terpenuhi")
    }
        reject("batal nonton")
    })
  }

async function asyncNonton() {
    try {
    let result = await nonton("jalan")
        console.log(result);
    } catch (error) {
        console.log(error)
    }
  }
  asyncNonton()

//Outputnya yaitu nonton terpenuhi
```
- Selain menggunakan async await,kita bisa juga menggunakan promise (then catch), namaPromis.then().catch(). Contoh scriptnya:
```
let nonton = (kondisi) => {
    return new Promise((resolve, reject) => {
      if (kondisi == "jalan") {
        resolve("nonton terpenuhi")
      }
      reject("batal nonton")
    })
  }
  nonton("jalan")
  .then(result => {
    console.log(result);
  }).catch(err => {
    console.log(err)
  })

//Output : nonton terpenuhi
```

### **Fetch**
- **Fetch** adalah mengirimkan network request dan juga bisa mengambil informasi data terbaru dari server jika dibutuhkan. Atau bisa juga diartikan native web API untuk melakukan HTTP calls dari external network. Contoh network request yang biasa dilakukan yaitu, mengirimkan data dari sebuah form, mengambil data untuk ditampilkan dalam list/table, serta mendapatkan notifikasi. Proses melakukan fetch() adalah salah satu proses asynchronous di JavaScript sehingga perlu menggunakan salah satu diantara promise atau async/await. Dalam fetch terdapat istilah JSON, Json adalah Javascript Object Notation atau mirip seperti object tetapi terdapat tanda kutip didalamnya.
- Fetch dengan promise. Contoh script :
```
 fetch("https://digimon-api.vercel.app/api/digimon")
  .then(result => result.json())
  .then(result => {
    console.log(result)
  })
```
- Fetch dengan async-await. Contoh script :
```
let getDataDigimon = async () => {
  let URL = "https://digimon-api.vercel.app/api/digimon"
  let response = await fetch(URL)
  let digimons = await response.json()
}

getDataDigimon()
```

## **Git dan Github Lanjutan**

### **Git dan Github**
- **Git** adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file. File -file yg disimpan menggunakan git akan terlacak seluruh perubahannya, termasuk siapa yang mengubah
- **Github** adalah platform khusus developer yang dibuat karena terinspirasi dari cara bekerja para programmer.
- Dalam git dan github lanjutan ini github digunakan untuk berkolaborasi antar anggota team dalam mengerjakan suatu project. Terdapat lebih dari satu orang mengerjakan tugasnya masing-masing, lalu diakhir nanti file tersebut akan digabungkan antara satu anggota dengan anggota yang lain. 
- Cara berkolaborasi dengan anggota kelompok, yaitu
  - Buat organization yang dibuat oleh team leader.
  - Invite anggota tim dan dijadikan owner.
  - Buat repo di organization. Repo dibuat public, dan ceklist Readme lalu buat branch dev.
  - Mengecek pull request. Setiap pull request, team lead akan mengecek, jika pull request belum selesai maka bisa diberikan komen atau kabar melalui pull request tersebut, jika sudah lalu lakukan merge. 
  - Aplikasi sudah selesai. Saat ini semua perubahan ada pada branch dev.
  - Jika tidak ada update terbaru dari developement, maka hubungkan antara branch dev dengan branch main. Lalu lakukan pull request untuk menggabungkan branch dev ke main.
- Yang dilakukan semua anggota team, yaitu :
  - Masing-masing anggota melakukan git clone pada reposit yang sudah dibuat dengan sebanyak satu kali saja.
  - Membagi tugas pada masing-masing anggota kelompok.
  - Pindah branch dev git switch dev.
  - Sebelum mencoding, lakukan git pull pada branch dev untuk update kode terbaru.
  - Anggota membuat branch dari dev git branch [nama-branch]
  - Pindah kedalam branch yang sudah dibuat, git switch [nama-branch]
  - Melakukan pengerjaan di dalam branch. 
  - Sebelum dipush, lakukan pindah ke branch dev lalu git pull dan git switch [nama-branch]
  - Selanjutnya,git merge dev untuk menghindari conflict.
  - Jika sudah aman, lakukan git commit lalu git push origin [nama-branch]
  - Lakukan pull request untuk merge ke branch dev.
  - Tunggu pull request diacc oleh team leader.

## **Responsive Web Design dan Boostrap 5**

### **Responsive Web Design**
- Responsive Web Design bertujuan membuat desain website yang dibuat dapat diakses dengan device apapun. Device yang digunakan biasanya adalah PC/Laptop, Smartphone, dan Tablet.
- Setiap developer website wajib menggunakan tools bawaan dari setiap browser yang mempermudah proses developement website. Pada browser chrome, biasa disebut Chrome Dev Tools. Akses chrome dev tools dapat menggunakan Ctrl+Shift+J saat sesudah membuka browser, maka responsive akan terlihat.
- **Viewport** adalah area website yang dapat diakses oleh user yaitu dari pojok kiri sampai dengan pojok kanan, pojok atas sampai pojok bawah.
- Viewport bisa dipasang pada website yang dibuat, dengan menggunakan meta viewport yang ada pada html. Viewport ini otomatis muncul saat kita menuliskan ement tanda seru pada html di vscode.
- Website yang tidak menggunakan viewport akan menyebabkan tampilan terlihat jauh saat diakses dalam layar smartphone. 
- **Max-Width** adalah kondisi dimana, gambar pada tampilan akan menjadi berapa persen dari ukuran layar. Hal ini dilakukan agar gambar tida terpotong saat responsive. Misalnya max-width : 100%, maka tampilan gambar menjadi 100% dari ukuran layar. Maka saat layar dikecilkan maka gambar akan menyesuaikan tampilan layar.
- **Satuan unit Relative** 
- Absolute Length terdiri dari :
  - cm
  - mm
  - in
  - px *
  - pt
  - pc 
- Relative Length terdiri dari :
  - em
  - ex
  - ch
  - rem
  - vw
  - vh
  - vmin
  - vmax
  - %
- Satuan unit relative yang sering dipakai adalah em, rem, vw, vh, %
- em vs rem. Em dan rem sama sama relative pada ukuran huruf. Rem, mengikuti ukuran huruf dari root element atau ukuran huruf paling awal. Em, mengikuti ukuran huruf dari element dimana dia berada. Root html atau ukuran font size html biasanya memiliki ukuran 16px. 
- vw vs vh. Vw adalah singkatan dari Viewport Width, sedangkan vh adalah singkatan dari Viewport Height. Misalnya jika fontsize 50vw, berarti element tersebut berukuran 50% dari ukuran lebar viewport, sedangkan jika fontsize 50vh, berarti element memiliki urukuran tinggi menyesuaikan atau mengambil lebar viewport sebanyak 50%. 
- **Media Query** adalah mengatur beberapa style yang tergantung jenis device yang digunakan. Dalam media query terdapat istilah breakpoint yang berarti patahan ketika layar dilebarkan lalu dikecilkan. 
- Media query untuk responsive web design umumnya menggunakan 2 jenis media query, yaitu max-width dan min-width.
- Terdapat 2 cara atau pattern dalam menggunakan media query, antara lain :
  - Membuat file css berbeda untuk masing-masing device. 
  - Menggabungkan 1 file css untuk setting styling berbagai device. 
- **Flex** yaitu setting website hanya bisa diatur satu arah, entah ke samping, ke atas, ataupun ke bawah.
- **Grid** , bisa setting secara vertikal ataupun horizontal. 

### **Boostrap 5**

Bootstrap adalah sebuah framework yang paling populer digunakan untuk membuat sebuah website. Bootstrap membuat front-end developer dapat membuat website dengan cepat, fokus pada responsive mobile, dan membuat website menjadi lebih interaktif tanpa membuat banyak CSS dan JavaScript dari nol.
Bootstrap 5 mengubah tampilan elemen checks & radios menjadi lebih modern serta menambahkan elemen switch checkbox untuk form Anda. Pada versi sebelumnya, tampilan elemen form di atas bisa berubah-ubah tergantung web browser yang digunakan. Hal tersebut membuat desain website Anda terkesan tidak konsisten.


- **Boostrap** adalah framework css yang digunakan untuk melakukan styling. Framework lain yaitu material.ui (mui.com), bulma, serta tailwind.
- Cara custom boostrap yaitu bisa langsung di element boostrapnya atau bisa juga ditimpa boostrapnya. 
- Cara menggunakan boostrap yaitu
  - Compile CSS dan JS.
  - Source file, didownload filenya lalu dipasang ke direktori website kita.
  - CDN via jsDelivr. Dan lain sebagainya.
- Pada boostrap terdapat beberapa komponen yang disediakan, yaitu :
  - Accordion
  - Alerts
  - Bagde
  - Breadcrumb
  - Buttons
  - Buttons group
  - Card
  - Carousel
  - Close button
  - Collapse
  - Dropdown
  - List group
  - Modal
  - Navbar
  - Navs & tabs
  - Offcanvas
  - Pagination
  - Placeholders
  - Popovers
  - Progress
  - Scrollspy
  - Spinners
  - Toast
  - Tooltips
- Selain itu juga terdapat beberapa cara untuk customize, layout, content, forms, helpers, utilities, extend, dan lain sebagainya. Bisa dilihat pada boostrap langsung. 
