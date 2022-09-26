# Summary <br> Kelas Web Development Basic

### MSIB Skilvul Minggu ke-6

<hr>

### Senin, 19 September 2022<br><br>
Materi : UNIX Command Line, dan Pengenalan GIT <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Command Line Interface (CLI)
Shell <br>
- Cara mengakses shell<br>
- File System Structure<br>
- Command untuk melihat current working directory<br>
- Command untuk melihat isi sebuah direktori<br>
- Command untuk berpindah direktori<br>
- Command untuk melihat isi dari files<br>
- Command untuk membuat file & direktori baru<br>
- Command untuk menyalin file & direktori<br>
- Command untuk memindahkan atau me-rename file & direktori<br>
- Command untuk menghapus file & direktori<br>

<br>

### <B>1. Pengertian CLI, Shell, dan Terminal Emulator </b> 
> - CLI atau Command Line Interface adalah sebuah jenis shell yang berbasis teks, ada pula contoh dari CLI yaitu Bash, SH, ZSH, CMD.exe
>- Shell merupakan program yang digunakan untuk berkomunikasi pada sebuah sistem.
>- Terminal Emulator adalah aplikasi yang berfungsi untuk mengakses CLI. 

### <B>2. Pengertian Filesystem</B>
> - Filesystem merupakan cara atau tata kelola bagaimana data diatur dan disimpan dalam filesystem.

### <b>3. Command untuk Navigasi </b>
> 1. <b>pwd</b> (Print Working Directory) <br>
     Command ini berfungsi untuk melihat <i>current working directory</i> atau posisi kita sedang membuka direktori apa dan dimana.
> 2. <b>ls</b> (lists) <br>
     Command yang berfungsi untuk melihat isi file yang ada pada sebuah direktori.
> 3. <b>cd</b> (change direktori) <br>
     Command yang berfungsi untuk berpindah direktori.

### <b>4. Manipulasi files dan Directory </b>
> 1. <b>head, tail, dan cat 
</b> <br>
     Command ini berfungsi untuk isi files di awal, akhir, dan keseluruhan.
> 2. <b>touch</b> <br>
     Command yang berfungsi untuk membuat file.
> 3. <b>mkdir</b> <br>
     Command yang berfungsi untuk membuat directory
> 4. <b>cp dan cp -R </b> <br>
     Command yang berfungsi untuk menyalin file (cp), dan untuk menyalin directory (cp -R).
> 5. <b>rm dan rm -R </b> <br>
     Command yang berfungsi untuk menghapus file (rm), untuk menghapus directory (rm -R / rm -d).
> 6. <b>mv dan mv -R </b> <br>
     Command yang berfungsi untuk memindahkan file (mv), untuk memindahkan directory (mv -R).


### <B>5. Pengenalan GIT</B>
> - Merupakan Tools untuk programmer yang berfungsi sebagai <i>version control system</i>
>- Git biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif. File -file yg disimpan menggunakan git akan terlacak seluruh perubahannya, termasuk siapa yang mengubah.

### <B>6. 3 kondisi file pada GIT</B>
> - <b>Modified</b> <br>
    Modified adalah kondisi dimana revisi atau perubahan sudah dilakukan, tetapi belum ditandai (untracked) dan belum disimpan dalam version control.
>- <b>Staged</b><br>
    Staged adalah kondisi dimana revisi sudah ditandai (modified) namun belum disimpan di version control.
>- <b>Comitted</b><br>
    Commit/committed adalah kondisi dimana revisi sudah disimpan pada version control.

### <B>7. Beberapa Command pada GIT</B>
> - git init (untuk inisialisasi)
> - git clone (untuk membuat local repository)
> - git status (untuk cek status)
> - git log (untuk melihat perubahan)
> - git branch (untuk melihat list branch)
> - git merge (untuk menyatukan file pekerjaan)

<br>

### Selasa, 20 September 2022<br><br>
Materi : HTML <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Mengetahui dan memahami kegunaan HTML pada web development
- Mengetahui cara menggunakan tools pendukung dalam HTML Development<br>
- Mengetahui cara membuat HTML sederhana<br>
- Mengetahui cara menjalankan HTML secara manual dan menggunakan live server<br>
- Mengetahui cara membaca dokumentasi HTML melalui w3schools<br>
- Mengetahui cara penggunaan Tag HTML yang populer<br>
- Mengetahui dan memahami semantic HTML<br>
- Mengetahui cara deployment HTML ke Netlify<br>

<br>

### <B>1. Pengertian HTML </b> 
> - HTML atau Hypertext Markup Language berfungsi untuk menampilkan konten pada browser. Contoh konten yang ditampilkan seperti text, audio, dan video.
> - HTML juga berfungsi sebagai kerangka dalam sebuah website.
> -  HTML bersifat statis dan hanya menampilkan konten yang diminta oleh developer.
> - HTML bukan sebuah bahasa pemrograman karena tidak bisa mengolaha data.

### <b>2. Tools yang dibutuhkan untuk membuat HTML</b>
>- Browser (contohnya seperti Microsoft Edge, Google Chrome, Mozilla Firefox, dll)
> - Code Editor (contohnya seperti VScode, Sublime Text, notepad++, dll)

### <b>3. Struktur HTML</b>
>- Pondasi utama dalam membuat HTML terdiri dari `<html><head><body></body></head></html>`.

### <b>4. HTML Anatomy</b>
>- Element
>- Opening tag
>- Content
>- Closing tag

### <b>5. Deploy HTML</b>
>- Deploy adalah sebuah proses untuk menyebarkan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang
>- Deploy HTML dapat menggunakan tools netlify

<br>

### Rabu, 21 September 2022<br><br>
Materi : CSS <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Apa itu CSS<br>
- Struktur CSS<br>
- CSS Comment<br>
- 3 Cara menggunakan CSS<br>
- Linking the CSS Files with HTML<br>
- Tag Name<br>
- Class Name<br>
- Multiple Classes<br>
- ID Name<br>
- Perbedaan Class Name dan ID Name<br>
- Chaining Selectors<br>
- Nested Element<br>
- !important pada CSS<br>
- Multiple Selector<br>
<br>

### <B>1. Pengertian CSS</b> 
> - CSS atau <i>Cascading Style Sheets</i> merupakan bahasa yang digunakan untuk mendesain atau mempercantik halaman sebuah <i>website</i>.
> - Dengan menggunakan CSS dapat mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya.

### <b>2. 3 cara menggunakan CSS</b>

> 1. **Inline styles**<br>
> Menambahkan CSS pada <i>attribute element</i> HTML<br>
> 2. **Menggunakan tag `<style></style>`**<br>
> 3. **.CSS Files**<br>
> Jika kita membutuhkan banyak code pada CSS, direkomendasikan untuk memisahkan code CSS di file tersendiri (extension .css) dan terpisah dari file HTML.

### <b>3. CSS tag name</b>
> - Kita bisa menggunakan Tag Elemen HTML secara langsung pada CSS. Jika menggunakan Tag Element, maka ini bersifat global.
>- Global artinya akan mempengaruhi seluruh Tag Elemen HTML yang ada pada file tersebut.

### <b>4. CSS - Class Name</b>
> - Kita bisa menggunakan attribute class pada elemen HTML lalu memanggil nama class tersebut pada CSS.
> - HTML yang memiliki class yang sama, akan mempunyai styling yang sama saat digunakan pada CSS.

### <b>5. CSS - Multiple Class</b>
> - Berfungsi untuk dapat menggunakan lebih dari 1 class yang berbeda untuk 1 element HTML

### <b>6. CSS - ID Name</b><br>
> - Berbeda dengan Class Name. ID Name bersifat unik artinya hanya ada 1 nama ID pada 1 element HTML.
> - Biasanya digunakan jika hanya ada 1 element pada 1 page. Contohnya navigation header dan footer.
> - Gunakan (#namaID) saat memanggil element ID HTML pada CSS

### <b>7. Perbedaan Class Name dan ID Name</b><br>
> - Berbeda dengan Class Name. ID Name bersifat unik artinya hanya ada 1 nama ID pada 1 element HTML.
> - Gunakan ID Name jika hanya ada 1 elemen pada file/halaman HTML. Contohnya navigation dan footer.
> - Gunakan Class Name jika akan ada beberapa element HTML yang memiliki styling/desain yang sama.

### <b>8. Chaining Selectors</b><br>
> -  Chaining selector dapat kita gunakan pada case/kasus berikut.
> - Jika memiliki 3 tag elemen HTML pada CSS namun ingin ada 1 elemen HTML yang memiliki styling berbeda.

### <b>9. Nested Element</b><br>
> - Konsep CSS sama dengan HTML yaitu setiap element memiliki parent dan child.

### <b>10. !important CSS</b><br>
> - !important CSS berada di level paling atas dari ID dan Class.<br>
> - Maksudnya adalah jika pada styling CSS kita menggunakan !important, maka styling sebelumnya baik itu ID Name atau Class Name akan di override.<br>

### <b>11. Multiple Selector</b> <br>
> Contoh sebelum dan setelah menggunakan Multiple Selecetor <br>

<b>Sebelum</b>
```css
h1{
font-size: 50px;
font-weight: 100;
color: blue;
}
p{
font-size: 50px;
font-weight: 100;
color: blue;
}
```
<b>Sesudah</b>
```css
p, h1{
font-size: 50px;
font-weight: 100;
color: blue;
}
```
### Kamis, 22 September 2022<br><br>
Materi : Algoritma dan Pengenalan Javascript <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Apa itu algoritma <br>
- Ciri-ciri Algoritma <br>
- Jenis proses Algoritma <br>
- 3 cara penyajian Algoritma <br>
- Mengenal dasar javascript <br>
<br>

### <B>1. Pengertian Algoritma</b> 
> - Algoritma merupakan proses langkah-langkah yang  dilakukan dengan cara logis (masuk akal) dan 
sistematis (terurut).

### <B>2. Ciri-ciri Algoritma</b> 
> 1. **input** <br>
     Memiliki 0 atau lebih input-an
> 2. **Output** <br>
     Memiliki minimal 1 output
> 3. **Definiteness** <br>
     Instruksi jelas dan tidak ambigu
> 4. **Finitenes** <br>
     Memiliki titik berhenti (stop)
> 5. **Effectiveness** <br>
     Sebisa mungkin tepat sasaran dan efisien

### <B>3. Jenis proses Algoritma</b> 
> 1. **Sequence** <br>
     Intruksi yang dijalankan secara berurutan.
> 2. **Selection** <br>
     Instruksi yg dijalankan jika memenuhi suatu kondisi.
> 3. **Iteration** <br>
     Instruksi yg berulang kali dijalankan selama memenuhi suatu kondisi.
> 4. **Concurrent** <br>
     Instruksi yg dijalankan secara bersamaan.

### <B>4. 3 cara penyajian Algoritma</b> 
> 1. **Deskriptif** <br>
     Penulisan algoritma dengan cara deskriptif seperti kita menulis tutorial (tata cara) dengan bahasa sehari-hari.
> 2. **Flowchart** <br>
     Flow chart atau diagram alir, penyajian algoritmanya lebih mudah dibaca karena memiliki tampilan visual. Flow chart menggunakan simbol bangun datar sebagai representasi dari proses yg dilakukan.
> 3. **Pseudecode** <br>
     Penulisan algoritma yg hampir menyerupai penulisan pada kode pemrograman disebut dengan pseudo code.

### <B>5. Pengertian Javascript</b> 
> - Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website.
> - Javascript juga dapat membuat website menjadi interaktif dan dinamis.

### <B>6. Syntax dan Statement</b> 
> - Syntax bisa dianalogikan seperti kosa kata (vocabulary) dan tata cara (grammar) pada bahasa pemograman.
> - Kita menggunakan syntax tertentu untuk membuat statement program, instruksi untuk djalankan/dieksekusi oleh web browser, compiler, ataupun intrepreter.

### <B>7. Tipe data</b> 
>  Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming. Javascript punya 6 tipe data fundamental, yaitu:
> - **number** <br>
     tipe data yang mengandung semua angka termasuk angka desimal.
> - **string** <br>
     grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya.
> - **boolean** <br>
     Tipe data yang hanya mempunyai 2 buah nilai.
     2 buah nilai tersebut adalah TRUE (benar) or FALSE (salah).
> - **null**<br>
     tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai.
> - **undefined**<br>
     tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai. Undefined berbeda dengan null.
> - **object**<br>
     Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya). <br>Tipe data object mempunyai key dan value.

### <B>8. Pengertian Variabel dan cara mendifinisikannya</b> 
>  Variable adalah container/tempat untuk menyimpan sebuah nilai, variabel dapat didefinisikan dengan 3 cara, yaitu:
> - **Var** <br>
> - **Let** <br>
> - **Const**<br>
     Variabel Const membuat data yang memiliki tipe const menjadi tidak bisa diubah nilainya.

### <B>9. Operator aritmatika pada Javascript </b> 
>  - `+` (penjumlahan)
>  - `-` (pengurangan)
>  - `*` (perkalian)
>  - `/` (pembagian)
>  - `//`(eksponen)
>  - `%` (modulus)
>  - `++` (increment)
>  - `--` (decrement)

### <b>10. Contoh penggunan operator aritmatika pada Javascript</b>
> `let a = 10;`<br>
> `let b = 5;`<br>
> `let hasil;`<br><br>
> `hasil = a+b;`<br><br>
> `console.log(hasil);`



<br>

### Jum'at, 23 September 2022<br><br>
Materi : Javascript Conditional<br> Mentor : Kak Dila <br>
Objective Learnings :
- Mengerti apa itu javascript conditional/percabangan <br>
- Mengerti apa itu looping pada javascript<br><br>

### <b>1. Apa itu javascript conditional?</b>
> - Conditional merupakan statement percabangan yang menggambarkan suatu kondisi. Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut. Jika kondisi True maka perintah akan dijalankan, jika False maka perintah tidak dijalankan.

### <b>Contoh Coonditional</b>
> - <b>IF Statement</b> <br>
> `let  lapar = true;`<br>
> `if (lapar){`<br>
> `console.log("Disarankan untuk makan);`<br>
> `};`<br><br>
> - <b>IF... ELSE Statement</b> <br>
> Else akan mengeksekusi sebuah statement/code jika suatu kondisi bernilai FALSE.<br>
> `let lapar = false;`<br>
> `if (lapar){`<br>
> `console.log("Disarankan untuk makan");`<br>
> `}else{`<br>
> `console.log("Tidak disarankan untuk makan");`<br><br>
> - <b>IF... ELSE IF Statement</b><br>
> Else … If statement dapat kita gunakan jika kita mempunyai berbagai kondisi.<br>
> `let lampulalulintas = hijau;`
> `if (lampulalulintas == 'merah'){`<br>
> `console.log("berhenti");`<br>
> `}else if (lampulalulintas == 'kuning'){`<br>
> `console.log("berhati-hati");`
> `}else if (lampulalulintas == 'hijau'{`<br>
> `console.log("Jalan");`<br>
> `else{`<br>
> `console.log("Error");`
> `};` <br><br>
> - <b>Truthy and Falsy</b><br>
> Analoginya adalah jika kita memiliki sebuah website dan meminta inputan username lalu menampilkannya. Jika usernamenya kosong kita bisa isi nilai tersebut.<br>
> `let nama = 'Ilham ganteng';`<br>
> `if (nama){`<br>
> `console.log(nama);`<br>
> `}else{`<br>
> `console.log('Variabel tidak ada');`<br>
> `};`<br><br>
> - <b>Truthy and Falsy Assignment</b><br>
> Analoginya adalah jika kita memiliki sebuah website dan meminta inputan username lalu menampilkannya. Jika usernamenya kosong kita bisa isi nilai tersebut.
> <br>`let defaultname;`<br>
> `if (username){`<br>
> `console.log(username);`<br>
> `}else{`<br>
> `defaultname == 'Stranger';` <br>
> `};`<br><br>
> - <b>Switch Case Conditional</b><br>
     Gunakan switch case jika kondisi dan percabangan terlalu banyak. <br>
> `var tombol = 1;`<br>
> `switch(tombol){`<br>
> `case 1:     { console.log("TransTV"); break; }` <br>
> `case 2:     { console.log("SCTV"); break; }` <br>
> `case 3:     { console.log("GlobalTV"); break; }` <br>
> `case 4:     { console.log("Spacetoon"); break; }` <br>
> `default:    { console.log("Stasiun TV belum ada!"); }`<br><br>
> - <b>Ternary Operator</b><br>
> Ternary operator merupakan short-syntax dari statement if … else.<br>
> `let AdaDiskon = true;`<br>
> `AdaDiskon ? console.log('ada diskon, ayo kita belanja!') : console.log('tidak ada diskon, jangan belanja!');` <br><br>

### <b>2. Apa itu Looping?</b>
> Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.<br><br>
> <b>Manual Looping</b> <br>
> `//Menampilkan angka 1-5`<br>
> `console.log('1');`<br>
> `console.log('2');`<br>
> `console.log('3');`<br>
> `console.log('4');`<br>
> `console.log('5');`<br><br>
> - <b>FOR LOOP</b><br>
> <b>Parameter</b><br>
> `for(initialization; condition; post-expression) {`<br>
> `// statements`<br>
> `}` <br>
> Inisialisasi: Sebagai inisialisasi awal dari mana mulainya sebuah pengulangan. Kita memberikan nilai awal/default pada parameter ini. <br>
Condition: For loop akan terus berjalan selama kondisi ini terpenuhi. Selama kondisi bernilai TRUE.<br>
Post-expression (Increment/Decrement): Iterasi statement yang digunakan untuk mengupdate variabel yang menjadi kontrol pada pengulangan.
> <b>contoh For Loop</b><br>
> `let angka = 1;`
> `for (angka; angka <= 5; angka++){`<br>
> `console.log(angka);`<br>
> `}` <br><br>
> - <b>WHILE LOOP</b><br>
     Gunakan WHILE LOOP jika kita tidak mengetahui jumlah pasti pengulangan.
> <b>Parameter</b><br>
> `while(expression){`<br>
> `//statement`<br>
> `}`<br>
> <b>contoh While Loop</b><br>
> `let angka = 1;`<br>
> `while(angka <= 5){`<br>
> `console.log(angka);`<br>
> `angka++;`<br>
> `}`<br><br>
> - <b>DO WHILE</b><br>
> <b>Paramater</b><br>
> `do{`<br>
> `statement (s);`<br>
> `} while(expression);`<br>
> While Do akan mengecek kondisi terlebih dahulu untuk mengulang blok kode. Sedangkan Do While akan mengulang blok kode baru mengecek kondisi.<br>
> <b>Perulangan While Do</b><br>
> `var bensin = 9;`<br>
> `while(bensin > 0){`<br>
> `console.log("Masih ada bensin, nyalan mesin!); `<br>
> `bensin--;`<br>
> `}`<br>
> <b>Perulangan Do While</b><br>
> `var bensin = 9;`<br>
> `do{`<br>
> `console.log("Nyalakan mesin!");`<br>
> `bensin--;`<br>
> `} while (bensin > 0);`<br><br>
> - <b>NESTED LOOP</b><br>
> Jika kita membuat looping didalam looping. Maka ini dinamakan Nested Loop. <br>Looping pertama dianalogikan sebagai baris.<br>Looping kedua dianalogikan sebagai kolom.
> <b>Contoh Nested Loop</b><br>
> `for (let i = 1; i <=5; i++){`<br>
> `for (let j = 1; j <=i; j++){`<br>
> `document.write('<br />')`<br>
> `document.write('baris', +i);`<br>
> `document.write('<br />')`<br>
> `document.write('kolom', +j);`<br>
> `}`<br>
> `}`<br>