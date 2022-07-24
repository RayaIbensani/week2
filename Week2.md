# WRITTING MINGGU 2
## JAVASCRIPT
### JavaScript
adalah bahasa pemograman yang sangat powerful yg digunakan untuk logic pada sebuah website
Javascript dijalankan melalui browser pada device setiap user.

### Cara menjalankan JavaScript
Kita mengakses JavaScript dengan element 

     <script src="script.js></script>
### Console log 
adalah temppat kita untuk cek logic pemograman web yang kita kembangkan
Console log juga tmpt kita untuk melakukan debugging (mengetahur error pada code) pada pemograman web

### Tipe data
adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalan programming
Ada 6 tipe data fundamental pada javaScript
1. Number(menggunakan nomor(12345/3,14))
2. string("...", '...')
3. Boolean(true/false)
4. null(nilai suatu variable yg kosong)
5. undefined(tidak terdefinisi)
* null biasanya diperoleh dalam kondisi normal dan sudah kita rencanakan,
undefined biasanya didapat dari kesalahan program (error), kelalaian programmer dan tidak direncanakan.
6. Object(data yg saling berhubungan, dpt menyimpan data dengan tipe data apapun, mempunyai key dan value)

### Operator
1. Assignment operator digunakan untuk menyimpan sebuah nilai pada variabel.
2. Increment dan Decrement digunakan untuk menambah atau mengurangi sebesar 1 nilai
3. Arithmetic Operator digunakan untuk operator yang melibatkan operasi matematika
* Tambah (+)
* Kuramg (-)
* Perkalian (*)
* Pembagian (/)
* Modulus (%) Modulus adalah hasil dari sisa bagi.
Misalkan 5 modulus 2. Hasil perkalian dari 2 yang mendekati 5 adalah 4. 
Maka sisa dari operasi modulus tersebut adalah 1.

4. Comparison Operator digunakan untuk membandingkan satu nilai dengan nilai lainnya. Hasil operasi yang melibatkan comparison operator adalah antara true or false. Simbol-simbol yang digunakan di Comparison Operator :
* Lebih kecil dari : <
* Lebih besar dari: >
* Lebih kecil atau sama dengan: <=
* Lebih besar atau sama dengan: >=
* Sama dengan: ===
Tidak sama dengan: !==

5. Logical operator biasa digunakan untuk sebuah CONDITIONAL pada pemograman.Menghasilkan nilai BOOLEAN yaitu TRUE or FALSE. Simbol dari Logical Operator sebagai berikut:
* AND operator : &&
* OR operator: ||
* NOT operator: !

### Conditional
Conditional merupakan statement percabangan yang   menggambarkan suatu kondisi yang akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut.

Yang dicek adalah apakah kondisi tersebut **TRUE** (benar), jika **TRUE** maka kondisi itu akan dijalankan.

* IF Statement
     
       if(true){
        console.log("Ini contoh IF Statement");
       }

* IF ELSE Statement,
Else akan mengeksekusi sebuah statement/code jika suatu kondisi bernilai **FALSE**

      let cerah = false
      If(cerah){
        console.log("main diluar")
      }else{
        console.log("diam dirumah")
      }
      Kondisi diatas tidak akan dijalankan karena bernilai false

* IF ELSE IF Statement
dijalankan jika memiliki berbagai kondisi

        let cuaca = "hujan"

        if(cuaca === "hujan"){
          console.log('Bawa payung');
        }
        else if(cuaca === "mendung"){
           console.log('Diam dirumah');
        }else{
           console.log('Healing time')
        }
        Kondisi yang akan ditampilkan adalah Bawa payung

* SWITCH CASE

      const browser = "firefox";
       switch (browser) {
       case "edge":
         console.log("Browser Anda tidak mendukung aplikasi ini");
       break;
       case "chrome":
       case "firefox":
          console.log("Browser Anda mendukung aplikasi ini");
        break;
        default:
          console.log("Semoga tampilan aplikasi ini cukup baik");
         }
     


### Looping
Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.

* FOR loop merupakan instruksi pengulangan yang dapat kita berikan pada program yang kita kembangkan. Gunakan FOR LOOP jika kita tahu seberapa banyak nilai pasti untuk pengulangannya.

      let N = 10;
      for (let i = 0; i <= N; i++) {
         console.log(i);
      outputnya adalah 1 - 10

* WHILE loop akan menjalankan instruksi pengulangan kondisi bernilai TRUE. Gunakan WHILE LOOP jika kita tidak mengetahui jumlah pasti pengulangan.

      let angka = 5
      while(angka <= 10){
       console.log(angka)
      angka++
      }
      outputnya adalah angka 5 sampai 10

* DO WHILE loop
 

       let number = 1
        do {
          console.log(number)
        number++
        } while (number <= 5);

* Nested loop
membuat looping didalam looping.

      for (let i = 1; i<=2; i++) {
         console.log('i -', i)
      for (let j = 1; j<=2; j++) {
         console.log('j -', j)
      }   console.log('luar -', i)
      }
    
## SCOPE & FUNCTION
### Scope
Scope adalah konsep dalam flow data variabel. 
Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.

**Blocks** adalah code yang berada didalam curly braces {}.
**Conditional, function, dan looping** menggunakan **blocks**.

* Global scope
 berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file.
Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks.
* Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping.
Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks.

### Function
Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.
Saat kita membutuhkan fitur tersebut nantinya, kita bisa kembali menggunakannya (kita bisa menggunakan 1 rumus untuk menyelesaikan beberapa masalah).

        function lingkaran(r) {
        return 3.14 * r ** 2;
        }
        function persegi(s) {
         return s ** 2;
        }
        console.log(lingkaran(10) + persegi(5));
        (r) & (s) adalah parameter, sedangkan (10) & (5) adalah argumen.(contoh fungsi luas lingkaran ditambah luas persegi)

* Default paramaters 
digunakan untuk memberikan nilai awal/default pada parameter function.
Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen.

       function myname (name = 'unknown'){
        return 'Hello ' + name;
       }
       console.log(myname('Fira'));
       console.log(myname());


## DOM MANIPULATION
DOM adalah singkatan dari Document Object Model. Penulisan atau penggunaan DOM diawali dengan document. Dengan adanya DOM ini, JavaScript diberi akses untuk membuat HTML menjadi dinamis, seperti:

* Mengubah element HTML pada halaman website.
* Mengubah attribute HTML pada halaman website.
* Mengubah CSS style pada halaman website.
* Menambah dan/atau menghapus element maupun attribute HTML.
* Menambah HTML event (contoh: efek klik pada mouse, hover pada mouse, dan lain-lain) pada halaman website.
* Berinteraksi dengan semua HTML event di website.

### InnerHTML
Element.innerHTML dapat kita gunakan untuk mengubah **konten** HTML di dalam sebuah element.
### Textcontent
Element.textContent dapat kita gunakan untuk mengubah **teks** di dalam sebuah element.

Perbandingan antar **innerhtml** dengan **textcontent** adalah jika kita menulis 

     <h1>Heading</h1> pada textcontent maka akan tertulis seperti itu juga pada webpage, berbeda dengan innerhtml yang langsung akan bertulis Heading pada webpage.

### .getelementByClassName
Selector yang mengambil semua TAG HTML dengan class name yang dicari

     <h1 class="header">ini contoh</h1>
     
     //Javascript
     let Classheader = document.getelementByClassName("header")


### .getelementById
Selector yang mengambil semua TAG HTML dengan Id yang dicari

     <div="header">ini contoh</h1>
     //Javascript
     let Classheader = document.getelementById("header")

### .querySelectorAll
Selector yang mengambil semua TAG HTML

     document.querySelectorAll("p") (untuk memanggil tag html p)
     document.querySelectorAll(.class)(untuk memanggil tag dengan attribut class)
     document.querySelectorAll(#Id)(untuk memanggil tag dengan attribut Id)
document.querySelector akan mengambil satu elemen saja,
sedangkan querySelectorAll akan mengambil semua elemen sehingga hasilnya berupa array.

## DOM Event
document object model yang bertugas untuk membantu interaksi user dengan document HTML.
1. mouse event
* Onclick untuk melakukan aksi klik

      <button id="klik">Hello</button>
      //Javascript
      buttonklik.onclick = showAlert
      maka yang akan muncul pada webpage adalah tombol Hello.

2. Blur
event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element)
       
       Enter your name <input id="username"/>
       // Javascript
       let input = document.getElementById('username')
       input.addEventListener('blur', () => {
	   if(input.value.length < 6) alert("Panjang username minimal 5")
       })
       maka jika kita mengklik bagian pada webpage maka akan keluar pop up tertulis panjang username minimal 5,kita juga bsa tidak memakainya.

3. Form
Event untuk membuat form pengisian data

       <form id="form">
       <input type=”email />
       <input type=”password”/>
       <br>(hanya untuk memberikan jarak)
       <button type="submit">Login</button>
       //javascript
        let form = document.getElementById("form")
        form.addEventListener('submit', function(event) {
	    event.preventDefault()
         console.log("submit")
	     const formData = new FormData(form)
        const values = Object.fromEntries(formData)
        })
        hasilnya akan seperti yang dibawah

<input type=”email /> <input type=”password”/>
<br>
<button type="submit">Login</button>

     









   

    