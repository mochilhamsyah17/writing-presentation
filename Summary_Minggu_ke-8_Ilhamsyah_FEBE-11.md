# Summary <br> Kelas Web Development Basic

### MSIB Skilvul Minggu ke-7

<hr>

### Senin, 3 Oktober 2022<br><br>
Materi : Javascript Array & Array Multidimensi <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami dan menggunakan struktur data Array <br>

<br>

### <B>1. Pengertian Array</b> 
> Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya.<br>
> Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.<br>
> Contoh Array
> ````javascript
> let toDoList = ['Bangun jam 8.30', 'Cuci Muka', 'Gosok gigi', 'Sarapan', 'Kelas Online jam 9'];
> console.log(toDoList);
> ````
>Sebuah Array di definisikan menggunakan Square Brackets
> ````javascript
> //square brackets
> []
> ````

<br>

### <b>2. Memanggil Array</b>
> - Array dihitung dari index data ke-0
> - Data pertama adalah index ke-0
> ````javascript
> let arr = [index0, index1, index2, index3];
> ````
> Jika kita ingin memanggil data ke 2, maka kita memanggil dengan cara seperti dibawah ini :
> ````javascript
> console.log(arr[1]); //output : index1
> ````
> Karena array dimulai dari 0, maka data ke 2 berada pada index ke-1, jika kita ingin memanggil data pertama maka index yang dipanggil adalah index ke-0 :
> ````javascript
> console.log(arr[0]); //output : index0
> ````

<br>

### <b>3. Update Array</b>
> Seperti tipe data dan variabel pada umumnya, kita dapat mengupdate data pada Array.
> Update array dapat dilakukan dengan cara seperti dibawah ini:
> ````javascript
> let angka = [1, 2, 3, 4, 5];
> angka[0] = 2;
> console.log(angka);
> //output : 2,2,3,4,5
> ````

<br>

### <b>4. Const pada Array</b>
> Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.
> ````javascript
> let motor = ['CBR', 'R15', 'GSX'];
> motor[1] = ['CB'];
> console.log(motor);
> //output : CBR, CB, GSX
> ````

<br>

### <b>5. Method pada array</b>
> Array memiliki method atau biasa disebut built-in methods. <br>
> Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan.<br>
> Contoh Array Built-in Methods
> - .push() <br>
> adalah method untuk menambahkan item  array pada urutan yang paling akhir.
> - .pop() <br>
> adalah method yang menghapus item array index terakhir.
> - .shift() <br>
> adalah method untuk menghapus item Array pada index pertama.
> - .unshift() <br> adalah method untuk menambahkan item Array pada index pertama.
> - .sort() <br> adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric.

<br>

### <b>6. Looping pada array</b>
> 1. .forEach() adalah method untuk melakukan looping pada setiap elemen array.
> ````javascript
> const motor = ['cbr', 'r15', 'gsx'];
> motor.forEach(element => {
>   console.log(element);
> });
> // output: cbr, r15, gsx
> ````
> 2. .map() melakukan perulangan/looping dengan membuat array baru.
> ````javascript
> let arr = [1,2,3,4,5];
> let doubled = arr.map(num =>{
>    return num*2;
> });
> console.log(doubled);
> //output : 2,4,6,8,10
> ````

<br>

### <b>7. Multidimensi Array</b>
> Multidimensional Array bisa dianalogikan dengan array of array.
> Ada array didalam array.
> ````javascript
> let laci = [
>   ['baju', 10],
>   ['celana', 10],
>   ['topi', 2];
> ];
> console.log(laci);
> ````
> Sama seperti array satu dimensi, multidimensional array juga dapat menggunakan Property dan Method built-in Array.

<br>

### Selasa, 4 Oktober 2022<br><br>
Materi : Javascript Object <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami dan menggunakan struktur data Object <br>
- Peserta mampu memahami dan menggunakan struktur data Array of Objects <br>

<br>

### <B>1. Pengertian Object, Properti, dan Method</b>
> 1. Object <br>
> sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method) 
> 2. Properti <br>
> data lengkap dari sebuah object.
> 3. Method <br>
> action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.

### <b>2. Membuat sebuah object</b>
> Object dapat diassign kedalam sebuah variabel dengan seperti dibawah ini:
> ````javascript
> let orang = {}; //orang is an empty object
> ````
> ````javascript
> let orang = {
>   nama: 'Ilhamsyah',
>   umur: 20,
>   isVerified: true;
> }
> ````
> Sama seperti array, didalam object kita dapat menyimpan properti dengan tipe data apapun.

### <b>3. Mengakses object dan properti object</b>
>````javascript
> let orang = {
>   nama: 'Ilhamsyah',
>   umur: 20,
>   isVerified: true;
> }
> console.log(orang);
> ````
> Dengan cara diatas merupakan cara mengakses seluruh object
>````javascript
> let orang = {
>   nama: 'Ilhamsyah',
>   umur: 20,
>   isVerified: true;
> }
> console.log(orang.name); //output : Ilhamsyah
> ````
> Dengan cara diatas merupakan cara mengakses properti object
> - Bracket Notation <br>
> Kita juga bisa menggunakan bracket notation saat memanggil properti dari sebuah object.
>````javascript
> let orang = {
>   nama: 'Ilhamsyah',
>   umur: 20,
>   isVerified: true;
> }
> console.log(orang['nama']); //output : Ilhamsyah
> ````

### <b>4. Update object</b>
> Kita dapat melakukan update pada variabel dengan tipe data Object.
>````javascript
> let orang = {
>   nama: 'Ilhamsyah',
>   umur: 20,
>   isVerified: true;
> }
> orang.umur = 17;
> orang.address = 'Bogor Utara, Bogor'
> console.log(orang);
> /*
> Output : 
> {
>   nama: 'Ilhamsyah',
>   umur: 17,
>   isVerified: true,
>   address = 'Bogor Utara, Bogor'
> }
> */
> ````

### <b>5. Menghapus properti object</b>
> Kita dapat menghapus properti dari object menggunakan delete operator.
>````javascript
> let orang = {
>   nama: 'Ilhamsyah',
>   umur: 20,
>   isVerified: true;
> }
> delete orang.umur;
> console.log(orang);
> /*
> Output : 
> {
>   nama: 'Ilhamsyah',
>   isVerified: true,
> }
> */
> ````

### <b>6. Method Object</b>
> Jika value yang kita masukkan pada property berupa function. Maka itu disebut method.
> <br>Kita akan membuat method untuk greeting pada aplikasi ecommerce misalnya.
> ````javascript
> const greeting = {
>    welcome: function(){
>        return 'Selamat datang';
>    },
>    afterTransaction: function(){
>        return 'Terima kasih';
>    },
> };
> console.log(greeting.welcome()); //output: Selamat datang
> ````

### <b>7. Nested Object</b>
> Pada real application nanti kalian pasti menemukan data object yang kompleks.
> Object yang berasal dari turunan object lainnya.
> ````javascript
> const news = {
>   title: 'Bogor hujan badai terus',
>   description: 'lorem ipsum 300 kali',
>   author: 
>       people:{
>               {
>               nama: 'Ilhamsyah',
>               umur: 20,
>               }
>              }
>  };
> console.log('News:', news.title);
> console.log('Articles Published by ', news.author.people.name);
> /* output:
>   News: Bogor hujan badai terus
>   Articles Published by Ilhamsyah
> */
> ````

### <b>8. Looping Object</b>
> Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping.
> <br>Jadi tidak perlu mengakses secara manual memanggil setiap propertinya.
> ````javascript
> for(let key in object){
>   //...
> }
> ````

### <b>9. Array of Object</b>
> ````javascript
> let siswa = [
>   {
>       nama: 'Ilhamsyah',
>       age: 20,
>   },
>   {
>       nama: 'Intan',
>       age: 20,
>   }
> ];
> //Gunakan forEach apabila object didalam array
> siswa.forEach((listSiswa) => {
>   console.log(listSiswa);
> });
> ````

<br>

### Rabu, 5 Oktober 2022<br><br>
Materi : Javascript Recursive <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
-  Peserta mampu memahami dan membuat program Rekursif <br>

<br>

### <B>1. Pengertian Rekursif</b>
> Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.
> <br> Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.

### <b>Struktur Rekursif</b>
> ````javascript
> function recursive () {
>   //..
>   recursive();
>   //..    
> }
> ````

### <b>2. Rekursif dengan conditional</b>
> ````javascript
> function recursive (){
>   if (condition){
>       //stop calling itself
>       //..
>   }else {
>           recursive();        
>   }
> }
> ````

### <b>3. Ciri-ciri rekursif</b>
> - Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
> - Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.

### <b>4. Contoh kasus rekursif</b>
> ````javascript
> function pow(x,n){
>   if (n == 1){
>       return x;
>   } else{
>       return x * pow (x, n-1);
>   }
> }
> console.log(pow(2, 3)); // output: 8
> ````

<br>

### Kamis, 6 Oktober 2022<br><br>
Materi : Javascript Asynchronus Introduction & Promise <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami proses Asynchronous pada JavaScript <br>

<br>

### <B>1. Pengertian Single Thread, Non-blocking, dan Asynchronus</b>
> 1. Single-thread
> <br> Proses yang dilakukan dengan menggunakan hanya 1 jalur, sehingga jika ada banyak proses yang terjadi akan saling menunggu dan mengantri dari atas kebawah.
> 2. Non-blocking
> <br> jika suatu tahap terlalu lama prosesnya, maka tahap tersebut akan mengizinkan tahapan selanjutnya untuk dieksekusi atau diproses terlebih dahulu.
> 3. Asynchronus
> <br> Merupakan proses yang dilakukan secara tidak berurutan.

### <b>2. 3 Kunci utama Asynchronus</b>
> 1. Callback
> <br> Merupakan fungsi yang meneruskan ke fungsi lain dengan harapan callback akan dipanggil pada waktku yang tepat. Callback juga dulunya merupakan cara utama penerapan fungsi asinkron dalam JavaScript.
> ````javascript
> function doStep1(init) {
>  return init + 1;
> }
>
> function doStep2(init) {
>  return init + 2;
> }
>
> function doStep3(init) {
>  return init + 3;
> }
>
> function doOperation() {
>  let result = 0;
>  result = doStep1(result);
>  result = doStep2(result);
>  result = doStep3(result);
>  console.log(`result: ${result}`);
> }
>
> doOperation();
>
> ````
> 2. Promise
> <br>Sebuah mekanisme baru pada fitur javascript / ES6 yang merepresentasikan sebuah object request pengolahan data yang dilakukan secara asynchronous seperti ajax, dan promise ini mewakili sebuah operasi yang belum selesai, tetapi diharapkan di masa mendatang.
> <br> Promise memiliki 3 keadaanm yaitu:
> - Pending
> - Fulfilled
> - Rejected
> ````javascript
>var isMomHappy = false;
>
>// Promise
>var willIGetNewPhone = new Promise(
>    function (resolve, reject) {
>        if (isMomHappy) {
>            var phone = {
>                brand: 'Samsung',
>                color: 'black'
>            };
>            resolve(phone); // fulfilled
>        } else {
>            var reason = new Error('mom is not happy');
>            reject(reason); // reject
>        }
>
>    }
>);
> ````
> Atau struktur dasar dari promise, seperti dibawah ini:
> ````javascript
> // promise syntax look like this
> new Promise(function (resolve, reject) { ... } );
> ````
> 3. Async Await
> <br>sebuah syntax khusus yang digunakan untuk menangani Promise agar penulisan code lebih efisien dan rapih. Async/Await terbagi menjadi Async dan Await, contohnya seperi dibawah ini: 
> ````javascript
> const getAllUser = async ()=> {
>	const data = await getUser()
>	console.log(data)
> }
> ````
> - Untuk menggunakan Async/Await, kembalian dari suatu fungsi harus merupakan suatu Promise. Async/Await tidak dapat berdiri tanpa adanya Promise.
> - Tidak seperti Promise, dengan Async/Await maka suatu baris kode dapat tersusun rapi mirip dengan kode yang sifatnya synchronous.
> - Setiap baris yang menggunakan await, akan ditunggu sampai Asynchronous Promise tersebut di resolve.

<br>

### Jum'at, 7 Oktober 2022<br><br>
Materi : Javascript Web storage <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami dan memanipulasi data menggunakan Web Storage <br>

<br>

### <B>1. Local Storage</b>
> Local storage memiliki 4 karakteristik, yaitu:
> 1. Menyimpan data tanpa tanggal kadaluarsa.
> 2. Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
> 3. Dapat menyimpan data hingga 5MB.
> 4. Hanya dapat menyimpan data string.<br>
> <br>
> 
> Untuk menyimpan data pada local storage, kita menggunakan method setItem() yang membutuhkan 2 parameter. Parameter pertama adalah key yang ingin kita simpan dan parameter kedua adalah data (value) dari key yang akan disimpan.
> ````javascript
> localStorage.setItem('key', value);
> ````
> Untuk mengambil data yang telah tersimpan pada local storage, kita dapat menggunakan method getItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang kita inginkan.
> ````javascript
> localStorage.getItem('key');
> ````
> Untuk menghapus data yang telah tersimpan pada local storage, kita dapat menggunakan method removeItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang ingin kita hapus.
> ````javascript
> // menghapus key tertentu
>localStorage.removeItem("key");
>
>// menghapus semua key
>localStorage.clear();
> ````

### <b>2. Session Storage</b>
> Berbeda dengan local storage, walaupun masuk ke dalam web storage, data yang tersimpan pada session storage akan hilang ketika session dari sebuah laman berakhir.
> <br> Session storage memiliki 5 karakteristik, yaitu
> 1. Data yang disimpan pada session storage akan terus tersimpan selama browser terbuka dan tidak hilang jika laman di-reload.
> 2. Membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window.
> 3. Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.
> 4. Data yang tersimpan dalam session storage harus berbentuk string.
> 5. Hanya dapat menyimpan data sebanyak 5MB.
> <br>
> <br>
> 
> Sintaks untuk menyimpan data pada session storage adalah sebagai berikut:
> ````javascript
> // menambah session storage
> sessionStorage.setItem('key', value);
> ````
> cara mendapatkan data dari session storage juga menggunakan getItem(), seperti berikut ini:
> ````javascript
> // mendapatkan session storage
> sessionStorage.getItem('key');
> ````
> Syntax untuk menghapus data dari session storage ada 2, yaitu:
> ````javascript
> // menghapus session storage satu persatu berdasarkan key
> sessionStorage.removeItem('key');
> 
> // menghapus seluruh session storage sekaligus
> sessionStorage.clear();
> ````