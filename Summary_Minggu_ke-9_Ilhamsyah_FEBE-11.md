# Summary <br> Kelas Web Development Basic

### MSIB Skilvul Minggu ke-9

<hr>

### Senin, 10 Oktober 2022<br><br>
Materi : Javascript Asynchronus Fetch & Await <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami proses Asynchronous pada JavaScript <br>
- Peserta mampu mengambil data API menggunakan fetch<br>

<br>

### <B>1. API</b> 
> API atau Application Programming Interface merupakan penghubung antara web-application dengan server.
> Perumpamaan-nya ialah API seperti pelayan (waitress) yang menghubungkan antara customer makanan disebuah restoran dengan koki yang berada di dapur.
> API biasanya berbentuk JSON (Javascript Object Notation).

<br>

### <b>2. Async Await</b>
> Async await merupakan syntax yang berfungsi untuk menangkap dari sebuah promise.
> Pada penulisan Async await terdapat 2 cara, yaitu dengan arrow function dan tidak menggunakan arrow function. <br>
> **ini menggunakan arrow function**
> ```javascript
> let asyncNonton = async() => { }
> ```
> **ini tanpa menggunakan arrow functon**
> ```javascript
> async function asyncNonton(){ }
> ```
> Async await dapat digunakan dengan syarat harus tedapat objek promise.
<br>

### <b>3. Penjelasan penggunaan Async Await</b>
> - Async/Await adalah salah satu cara untuk mengatasai masalah asynchronous pada Javascript selain menggunakan callback dan promise.
> - Pada implementasi Async/Await, kita menggunakan kata kunci async sebelum fungsi. Await sendiri hanya bisa digunakan pada fungsi yang menggunakan async.
> - Untuk menggunakan Async/Await, kembalian dari suatu fungsi harus merupakan suatu Promise. Async/Await tidak dapat berdiri tanpa adanya Promise.
> - Tidak seperti Promise, dengan Async/Await maka suatu baris kode dapat tersusun rapi mirip dengan kode yang sifatnya synchronous.
> - Setiap baris yang menggunakan await, akan ditunggu sampai Asynchronous Promise tersebut di resolve.
<br>

### <b>4. Fetch</b>
> Fetch merupakan proses pengambilan data. Pada sebuah API yang memiliki data dapat kita ambil menggunakan fetch. Karena API biasanya mengandung atau menggunakan bahasa JSON, maka dengan menggunakan fetch akan melakukan pembongkaran atau unboxing dari JSON tersebut biasanya menjadi sebuah array object.
> ```javascript
> fetch('products.json')
>  .then((response) => {
>    if (!response.ok) {
>      throw new Error(`HTTP error: ${response.status}`);
>    }
>    return response.json();
>  })
>  .then((json) => initialize(json))
>  .catch((err) => console.error(`Fetch problem: ${err.message}`));
> ```

<br>

### Selasa, 11 Oktober 2022<br><br>
Materi : Git dan GitHub Lanjutan <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :
- Peserta mampu memahami kenapa Git dan Github tools yang wajib digunakan <br>
- Peserta mampu memahami perbedaan antara Git dan Github<br>
- Peserta mampu memahami alur kerja dari Git dan Github<br>
- Peserta mampu memahami dan membuat Repository Git<br>
- Peserta mampu melakukan commit pada Git<br>
- Peserta mampu melakukan merge pada Git<br>
- Peserta mampu menyelesaikan conflict pada Git<br>
- Peserta mampu mempublish aplikasi ke Github<br>

<br>

### <b>1. GIT Branch</b>
> GIT branch berfungsi untuk membuat cabang baru dari cabang master(utama) yang mana berfungsi untuk meminimalisir terjadinya konflik ketika kerja sama tim.
> Membuat branch baru tidak akan mengganggu file yang berada pada cabang utama(master). Sehingga aman.

<br>

### <b>2. Syntax GIT branch</b>
> - Git branch <br> berfungsi untuk melihat list brang yang ada
> - Git Checkout <br> berfungsi untuk pindah ke brach tertentu.
> - Git branch -d ```<branch>``` <br> berfungsi untuk menghapus branch tertentu.

<br>

### <b>3. Git Merge</b>
> Git merge berfungsi untuk menyatukan branch yang sudah dibuat, dengan tahapan seperti dibawah ini.
> ```github
> # start new feature
> git checkout -b fitur-baru master
> # edit some files
> git add <file>
> git commit -m "mulai fitur baru"
> # edit some files
> git add <file>
> git commit -m "fitur baru selesai"
> # merge in the fitur-baru branch
> git checkout master
> git merge fitur-baru
> git branch -d fitur-baru
> ```

<br>

### Rabu, 12 Oktober 2022<br><br>
Materi : Responsive web & Bootstrap <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings : 
- Peserta mampu memahami apa itu Responsive Web Design<br>
- Peserta mampu menggunakan tools untuk membuat website yang responsif<br>
- Peserta mampu memahami dan menggunaka viewport<br>
- Peserta mampu memahami dan menerapkan Relative CSS Unit<br>
- Peserta mampu memahami dan menggunakan Media Query
- Peserta mampu memahami dan menggunakan Flexbox dan Grid<br>
- Peserta mampu memahami mengapa dan kapan menggunakan Bootstrap<br>
- Peserta mampu memahami dan menggunakan layout pada Bootstrap<br>
- Peserta mampu memahami dan menggunakan content pada Bootstrap<br>
- Peserta mampu memahami dan mengunakan component pada Bootstrap<br>
- Peserta mampu membuat website responsif menggunakan Bootstrap <br>

<br>

### <b>1. Apa itu responsive</b>
> Responsive Web merupakan display dari sebuah web yang tampilannya mengikuti dengan ukuran layar sebuah device. Sehingga website dapat diakses oleh device apapun.

### <b>2. Viewport?</b>
> Viewport merupakan area yang dapat dilihat oleh user.
> ```html
> <meta name="viewport" content="width=device-width, initial-scale=1.0">
> ```

### <b>3. Media Query</b>
> Media Query digunakan untuk membuat beberapa styles tergantung pada jenis device.
> Jenis-jenis media Query antara lain:<br>
> - min-width
> - max-width
> <br>

### <b>4. 2 Cara penggunaan media query</b>
> - Cara ke-1 <br> Membuat file CSS berbeda untuk masing-masing device
> - Cara ke-2 <br> Menggabungkan 1 file CSS untuk setting styling berbagai device.

### <b>5. Breakpoint</b>
> Adalah perubahan yang terjadi pada tampilan saat berganti device atau ukuran width.

### <b>6. Flexbox </b>
> Flexbox atau Flexible Box  merupakan sebuah mode pengaturan atau konsep layout pada CSS yang digunakan untuk mengatur elemen atau container beserta item didalamnya pada halaman web. <br>
> - Justify Content dan Align Items
> Justify-content dan align-items adalah dua properti CSS yang membantu kita mendistribusikan item-item di dalam container. Mereka mengontrol bagaimana item diposisikan secara horizontal (main axis) maupun vertikal (cross axis).
> ```css
> .container {
>     display: flex;
>     justify-content: space-between;
> }
> ```
> Selain center kita juga bisa menggunakan space_between yang akan memberikan jarak antar item sebagai berikut:

> ```css
> .container {
>     display: flex;
>     justify-content: space-between;
> }
> ```
> Berikut ini beberapa nilai lain yang bisa dipakai untuk justify-content:
> - flex-start (default)
> - flex-end
> - center
> - space-between
> - space-around
> - space-evenly <br>
> - Mengontrol Satu Item
> Selain mengontrol beberapa item secara bersamaan menggunakan teknik yang sebelumnya sudah kita bahas, kita juga bisa mengontrol hanya satu item saja. Misal, kita ingin membuat dua item pertama di sebelah kiri, namun menggeser item logout ke sebelah kanan. <br>
> Untuk melakukan hal tersebut ada sebuah teknik lama, yaitu dengan mengatur margin-nya menjadi auto.
> ```css
> .logout {
>     margin-left: auto;
> }
> ```

  ### <b>7. Boostrap </b>
> Bootstrap adalah framework CSS yang bersifat Free dan Open Source. Bootstrap menyediakan class-class CSS dan beberapa fungsi Javascript untuk mempermudah pembuatan web. <br>
> Kita dapat menggunakan bootstrap dengan mendownload filenya, dan menaruh file tersebut pada folder project kita dan di link pada file html yang akan digunakan:
> ```css
> <link rel="stylesheet" href="css/bootstrap.min.css" />
> ```
