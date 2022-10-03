# Summary <br> Kelas Web Development Basic

### MSIB Skilvul Minggu ke-7

<hr>

### Senin, 26 September 2022<br><br>
Materi : Javascript scope & function <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami scope <br>
- Peserta mampu memahami dan membuat fungsi<br>
- Peserta mampu menghadapi dan menyelesaikan error serta bug<br>

<br>

### <B>1. Pengertian dari Scope pada Javascript</b> 
> - Scope merupakan konsep dalam flow data variabel yang menentukan suatu variabel bisa diakses atau tidaknya.
> - Contoh analoginya adalah jika kita berada di Bogor, maka kita tidak bisa melihat Kebun raya yang berada di Kota Bogor jika kita sedang berada di Sukabumi, karena Kebun raya bersifat local yang berada hanya di Kota Bogor.

### <B>2. Pengertian Blocks</B>
> - Blocks merupakan code yang berada didalam curly { }.
> - Contoh dari penggunaan blocks seperti pada looping, function, dan percabangan(conditional).

### <b>3. Pengertian Global scope </b>
> - Global scope merupakan variabel yang dibuat untuk dapat diakses dimanapun pada suatu file.
> - Persyaratan agar variabel dapat diakses secara global dengan cara variabel harus dideklarasikan di luar blocks. Berikut Contoh Script Variabel yang dideklarasikan secara global scope.
> ```javascript
> let nama = 'ilhamganteng';
> function fact(){
>    return fact; //didalam blocks
> }
> console.log(nama); //print ilhamganteng
>```

### <b>4. Pengertian Local scope </b>
> - Local scope berarti mendeklarasikan variabel dalam <u>blocks</u> seperti function, looping, conditional.
> - Variabel yang berada pada local scope hanya dapat diakses didalam blocks tersebut. Contoh dari local scope seperti diabawah ini
> ```javascript
> function fact(){
>    let nama = `ilhamganteng`; //didalam blocks
>    return nama; 
> }
> console.log(fact()); // print ilhamganteng
> console.log(nama); //error karena variabel nama berada di dalem blocks (bukan global scope)
> ```
> - Jadi dapat disimpulkan bahwa jika ingin memanggil variabel yang berada di local scope harus memanggil funciton atau local yang menampung variabel tersebut terlebih dahulu.

### <b>5. Pengertian Function pada Javascript </b>
> - Function merupakan sebuah blok kode dalam sebuah grup yang berfungsi untuk menyelesaikan 1 task/ 1 fitur.
> - contoh pembuatan function
> ```javascript
> function realll(){
>    return 'ilham keren'; //print ilham keren
> }
> ```
> - Struktur Function, seperti dibawah ini
> ```javascript
> function /*merupakan function keyword*/ realll() /*identifier*/{
> return 'ilham keren'; //merupakan function body
> }
> ```
### <b>6. Cara memanggil Function pada Javascript </b>
> - Cara memanggil function dengan cara dibawah ini
> ```javascript
> realll() //memanggil function
> console.log(realll()); //menampilkan isi dari function tersebut.
> ```
### <b>7. Pengertian Parameter dan Argumen </b>
> 1. Parameter <br>
> Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.
Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut. Contoh Parameter Function yaitu seperti dibawah ini:
> ```javascript
> function apaja(parameter1, parameter2){
> console.log(varparameter1,varparameter2);
> }
> ```
> 2. Argumen<br>
> Argumen adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah parameternya Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen.
> ```javascript
> function perkalian(parameter1, parameter2){
> return parameter1 * parameter2;
> }
> console.log(perkalian(1,2)) //(1,2) merupakan nilai argumen
> ```
### <b>7. Pengertian Default Parameter </b>
> - Default Parameter digunakan untuk memberikan nilai awal/default pada parameter function.
> - Default Parameter berfungsi untuk menjaga function agar tidak error saat dipanggil tanpa argumen. <br> Contoh Default Parameter ialah:
> ```javascript
> function tanggalLahir(umur = '17'){
> return 'Umur kamu ' + umur + 'tahun';
> }
> console.log(tanggalLahir('20')); //Output : Umur kamu 20 tahun
> console.log(tanggalLahir()); //Output : Umur kamu adalah 17 tahun
> ```
### <b>8. Pengertian Function Helper </b>
> - Function helper berfungsi untuk menggunakan function lain kedalam sebuah function. Contohnya
> ```javascript
> function perkalianSembilanPerLima(number){
>    return number * (9/5); 
>};
> function getFahrenheit(celcius){
>    return perkalianSembilanPerLima(celcius) + 32;
> };
> getFahrenheit(15); //Output : 59
> ```
>### <b>9. Arrow Function </b>
> - Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version). Contohnya seperti dibawah ini:
> ```javascript
> const pembagian = (angka1,angka2) => {
>    return angka1/angka2;
> }
> ```
<br>

### Selasa, 27 September 2022<br><br>
Materi : Data Type Built in Prototype & Method <br> Mentor : Kak Auzan Assidqi <br>

<br>

### <B>1. Tipe data yang berada pada Javascript</b> 
> - Tipe Data Primitive
> - - Boolean <br>Tipe data ini mempresentasikan logika yang terdiri dari ***true*** dan ***false***. Tipe data ini biasanya digunakan untuk memverifikasi saja. <br>
> - - Null type <br> Tipe data ini mempresentasikan bahwa tipe data ini tidak ada isinya atau null.
> - - Undefined <br> Tipe data ini mempresentasikan sebuah variabel tidak ada isinya, berbeda dengan null, Undefined akan ada jikalau ada error.
> - - Numeric <br> Tipe data ini memiliki tipe data berupa number atau BigInt
> - - Number <br> Tipe data ini berupa nomor yang memiliki nilai minimum dan maksimal.

### <b>2. Apa itu Tipe data String</b>
> - Tipe data string merupakan tipe data yang terdiri dari apapun yang ada pada keyboard kita, baik number ataupun huruf.<br> Cara untuk menggunakan tipe data string pada JS yaitu:
> ```javascript
> const string1 = 'Ilhamsyah Maulana'
> ```

### <b>3. Transformasi tipe data string</b>
> - toUpperCase() <br> Transform ini berfungsi untuk merubah nilai string yang ada pada sebuah variabel menjadi kapital semua. Contoh
> ```javascript
> let string1 = 'Ilhamsyah Maulana'
> console.log(string1.toUpperCase())// Output : ILHAMSYAH MAULANA
> ```
> - toLowerCase() <br> Transform ini berfungsi untuk merubak nilai string pada sebuah variabel menjadi huruf kecil semua. Contoh
> ```javascript
> let string1 = 'Ilhamsyah Maulana'
> console.log(string1.toLowerCase())// Output : ilhamsyah maulana
> ```
> 
### <b>4. MATH</b>
>- Math merupakan method yang memiliki properti yang biasa digunakan untuk matematika constant dan function. Math dapat digunakan dengan tipe data Number dan tidak dapat digunakan dengan tipe data BigInt.
> - Terdapat beberapa Math properties, contohnya
> <br>Math.E, Math.LN2, Math.LN10, Math.LOG2E, Math.LOG10E, dan lain-lain.
> - Pada Math juga terdapat method, contohnya seperti
> <br> Math.abs(), Math.sqrt(), Math.ashin(), Math.asin, dan lain-lain.

### <b>5. Tipe data Non-Primitve</b>
>- Tipe data non-primitive adalah tipe data yang dapat menyimpan lebih dari satu nilai pada satu waktu dan dapat diubah. Tipe data non-primitif akan dianggap berbeda meskipun nilainya sama dan dalam urutan yang sama. Tipe data Non-Primitive adalah Object. 

<br>

### Rabu, 28 September 2022<br><br>
Materi : Javascript DOM Intorduction<br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami dan memanipulasi konten HTML dengan DOM<br>
<br>

### <B>1. Pengertian DOM</b> 
> - DOM (Document Object Manipulation) merupakan representasi dokumen yang memungkinkan Javascript dapat mengakses dan memanipulasi elemen dan style pada website, atau
> - DOM juga merupakan jembatan untuk bahasa pemrograman dapat berinteraksi dengan dokumen HTML.
> - Kesimpulan, DOM berfungsi untuk membuat Javascript dapat memanipulasi HTML.

### <b>2. Mencari elemen HTML</b>
> <b>TRAVERSING</b>
> - <b>KeBawah</b>
> - - Mencari element berdasarkan element Id, dengan cara seperti dibawah ini
> ```javascript
> document.getElementById(id);
> ```
> - Mencari element berdasarkan element Class, dengan cara seperti dibawah ini
> ```javascript
> document.getElementByClass(name);
> ```
> - Mencari element berdasarkan element tag name, dengan cara seperti dibawah ini
> ```javascript
> document.getElementByTagName(name);
> ```
> - <b>Keatas</b>
> - - Untuk mengakses parent dapat menggunakan:
> ```javascript
> itemQuery.parentElement;
> itemQuery.closest(". ");
> ```
> - <b>Kesamping</b>
> - - Untuk mengakses sibling dapat menggunakan:
> ```javascript
> itemQuery.previousElementSiblingc;
> itemQuery.nextElementSibling;
> ```


### Kamis, 29 September 2022<br><br>
Materi : DOM Manipulation <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami dan memanipulasi konten HTML dengan DOM <br>
<br>

### <B>1. Perbedaan innerHtml dan innerText </b> 
> 1. Pengertian innerHtml
> <br> innerHtml menampilkan content dari element saja, misalnya
> ```javascript
> ilham.innerHtml = "<h1>Haluww</h1>"
> ``` 
> Maka yang ditampilkan adalah ``Haluww``. Perbeda dengan innerText yang akan ilham jelaskan dibawah ini.
> 2. Pengertian innerText
> <br> innerText menampilkan element, misalnya
> ```javascript
> ilham.innerHtml = "<h1>Haluww</h1>"
> ``` 
> Maka yang ditampilkan adalah ``<h1>Haluww</h1>``

### <B>2. Append() dan AppendChild() </b>
> 1. Append()
> <br>Append() berfungsi untuk menambahkan sebuah elemen baru tanpa harus menyertakan element tersebut di tag HTML. Cara kerja dari fungsi append() adalah dimana ketika website diakses maka akan menambahkan element baru pada html melalui fungsi tersebut. misalnya
> ```javascript
> let p = document.createElement("p")
> p.innerText = "ini adalah paragraf"
>ilham.append(p) //akan mencetak ini adalah paragraf di baris id ilham
> ```
> 2. AppendChild()
> <br>AppendChild() berfungsi untuk menambahkan elemen baru tetapi berbeda dengan Append(), AppendChild() hanya menambahkan elemen baru berupa Node Object dan tidak bisa berupa DOMstring.

### <b>3. Remove()</b>
> Remove berfungsi untuk menghapus element node dari sebuah dokumen.

### <b>4. getAttribute() dan setAttribute()</b>
> getAttribute() berfungsi untuk mengembalikan nilai atribut tertentu pada element HTML. Contoh data atribut data-color pada button.
> Sedangkan setAttribute akan mengatur class yang ada. Misalkan
> ```html
> <!DOCTYPE html>
> <html>
> <style>
>.democlass {
>  color: green;
>}
></style>
>
><body>
>><h1 id="myH1">The Element Object</h1>
><h2>The setAttribute() Method</h2>
>
><p>Click "Add Class" to add a class attribute to the h1 element:</p>
>
><button onclick="myFunction()">Add Class</button>
>
><script>
>function myFunction() {
>  document.getElementById("myH1").setAttribute("class","democlass"); 
>}
></script>
>
></body>
></html>
> ```
> Dengan code diatas, maka akan mengubah warna h1 sesuai yang telah disetting jikalau ditekan tombol add class.
> 

<br>

### Jum'at, 30 September 2022<br><br>
Materi : DOM Events<br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami dan memanipulasi konten HTML dengan DOM<br><br>

### <b>1. Apa itu Events</b>
> - Events merupakan segala kejadian/kegiatan/interaksi yang terjadi pada website.
> - Events terdiri dari 7 tipe, yaitu :
> - - click
> - - submit
> - - focus
> - - blur
> - - hover
> - - change
> - - scroll<br><br>
> - events dapat diberikan dengan 3 cara, yaitu
> - - HTML attribute
> - - event property
> - - addEventListener()

### <b>2. Contoh menggunakan event pada website dengan 3 cara</b>

> Cara 1 (HTML attribute)<br>
> ```html
> <h1 onclick="alert('Selamat Datang')">Hallo</h1>
> ```
> Cara 2 (event property)
> ```javascript
> paragraf.onclick = function(){
> alert("Ini adalah paragraf");
> }
> function tampilkanAlert(){
>   alert("ini alert ya ges ya")
> }
> ```
> Cara 3 (addEventListener)
> ```javascript
> let button = document.getElementById("btn")
> button.addEventListener("click", function(){
>    alert("ini dari button")
> })
> ```
### <b>3. EventListener</b>
> - Click
> <br> Misalkan kita mempunyai element 
> ```html
> <input id=”user-input” />  dan <button id=alert-button”>show</button>. 
>```
>Kita ingin menampilkan pop up box yang berisi teks di dalam input tadi.
> - Blur
> <br> “Blur”, lawan dari “focus”, adalah event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element)
> ```javascript
> // cari dulu element tersebut berdasarkan id-nya
> const input = document.getElementById(“username”)
> // tambahkan event listener
> input.addEventListener(“blur”, () => {
>	if(input.value.length < 6) alert(“Panjang
> username minimal 6”)
> })
> ```
> - Form Submission
> <br> Misalkan kita mempunyai element beberapa input dalam sebuah form 
> ```html
> <input name=”email /> dan <input type=”password” name=”password” />
> ``` 
> Bagaimana caranya  kita mendapatkan isi dari kedua input tersebut saat submit form? Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input