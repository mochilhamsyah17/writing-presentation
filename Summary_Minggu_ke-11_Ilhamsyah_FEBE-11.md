# Summary <br> Kelas Web Development Basic

### MSIB Skilvul Minggu ke-11

<hr>

### Senin, 24 Oktober 2022<br><br>

Materi : Intro React JS and Installation <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :

- Peserta mampu memahami React.js secara fundamental <br>
- Peserta mampu menjalankan aplikasi React.js

<br>

### <B>1. Apa itu React JS ?</b>

> React JS merupakan sebuah framework view library Javascript yang berfungsi untuk membuat tampilan (user interface) pada website.
> React JS dibuat oleh time engineer Facebook.
> React JS digunakan oleh facebook pada sisi Front-End
> <br>

### <b>2. Mengapa menggunakan React JS ?</b>

> - React JS is Modular <br> React JS dapat membagi 1 tmapilan pada website menjadi komponen-komponen kecil.
> - React JS is FAST <br> Dengan menggunakan React JS dapat membuat aplikasi Front-end menjadi lebih cepat meskipun wajib menghandle berbagai data.
> - React JS is Scalable <br> React JS dapat digunakan pada aplikasi berskala kecil hingga berskala besar dan kompleks.
> - React JS is Popular <br> Kebanyakan perusahan teknologi menggunakan React JS, sehingga dapat memudahkan mencari pekerjaan, freelance, bahkan startup jika menggunakan React JS.

### <b>3. Instalasi React JS</b>

> 1. Install Node JS
> 2. Pada Git Bash, buat folder atau tempat untuk menginstall dan download react js
> 3. install react js dengan menggunakan:
>
> ```bash
> npx create-react-app my-app
> ```
>
> 4. Akses React menggunakan localhost:3000

### <b>4. Perbandingan membuat UI Elements React JS vs Vanilla JS</b>

> - Vanilla Javascript
>
> ```javascript
> // membuat DOM
> const rootElement = document.getElementById("root");
> // membuat element baru
> const element = document.createElement("div");
> // membuat content dan class
> element.textContent = "Hello World";
> element.className = "Container";
> //memanggil elemn baru dibawah rootElement
> rootElement.appenChild(element);
> ```
>
> VS <br>
> React JS
> <br>
>
> 1. Membuat file HelloWorld.js di directory /src, dengan isi sebagai berikut:
>
> ```javascript
> import react from 'react';
> //membuat element UI komponen baru berisi text hello world
> function HelloWorld(){
>   return{
>       <h1>Hello World</h1>
>   }
> };
> //export element
> export default HelloWorld;
> ```
>
> 2. Edit file App.js dengan menambahkan panggilan untuk hello world
>
> ```javascript
> import react from "react";
> //import komponen elemen hello world
> import HelloWorld from "./HelloWorld";
> function App() {
>   return (
>     <div>
>       //memanggil elemen ke root App
>       <HelloWorld />
>     </div>
>   );
> }
> export default App;
> ```

### <b>5. JSX</b>

> JSX merupakan syntax extension untuk Javascript yang digunakan untuk react JS.
> <br> JSX juga berfungsi untuk dapat menggunakan HTML didalam file ekstensi javascript (.js).
> <br> JSX memiliki beberapa peraturan, yaitu:
>
> 1. Setiap JSX hanya memiliki 1 parent element dan tidak boleh lebih.
> 2. Gunakan `<div>` sebagai parent dari element lain pada komponen
> 3. Bisa juga menggunakan tag fragment `<>`

<br>
<br>

### Selasa, 25 Oktober 2022<br><br>

Materi : React JS Component <br> Mentor : Kak Dila <br>
Objective Learnings :

- Peserta mampu memahami dan membuat component pada React.js
- Peserta mampu memahami dan menggunakan JSX
- Peserta mampu membedakan class component dan functional component

<br>

### <b>1. Apa itu Component ?</b>

> Component merupakan satu core dari React JS yang dapat membagi UI dalam satuan-satuan kecil, yang mana artinya dalam 1 page terdapat beberapa component yang dibuat. <br><br>
> Component dibuat jika component tersebut bersifat reusabel code atau jika skala project, component tersebut dibutuhkan pada section atau page lain. Sehingga component yang dibuat dapat digunakan pada page lain juga.

### <b>2. Bagaimana membuat Component ?</b>

> - Menggunakan function
> - Menggunakan class
>   <br> Kebanyakan kasus dan dokumentasi resmi react JS dirokemendasikan menggunakan function.

### <b>3. Memanggil CSS pada react</b>

> ```javascript
> import "./App.css";
>
> function App(){
>   return(
>       <>
>           <div className = "profile-container">
>               <img src="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2022/03/08055643/Cari-Dokter-Umum-Terbaik-di-Yogyakarta_-Ini-5-Rekomendasinya.jpg" className="profile-img">
>               <div>
>               <h2>Ilhamsyah</h2>
>               <h3>20 Tahun</h3>
>               <p>Peserta Bootcamp FrontEnd Skilvul</p>
>               </div>
>           </div>
>       </>
>   );
> };
> ```
>
> Bisa dilihat pada code diatas, kita perlu membuat file css terlebih dahulu dan melakukan pemanggilan dengan menggunakan import "(alamat file css)"; <br>
> Lalu juga yang membedakan dari react js dan html itu pada pemanggilan class css. Pada html memanggil dengan menggunakan class="..", sedangkan pada react berganti nama menjadi className=".."

### <b>4. Cara membuat props menjadi static</b>

> 1. buat file baru pada components, kali ini membuat MemberInfo.jsx
> 2. isi code memberinfo seperi dibawah ini:
>
> ```javascript
> function MemberInfo = ({name, age, info, imgUrl}) => {
>   return(
>       <>
>           <div className = "profile-container">
>               <img src={imgUrl} className="profile-img">
>               <div>
>               <h2>{name}</h2>
>               <h3>{age}</h3>
>               <p>{info}</p>
>               </div>
>           </div>
>       </>
>   );
> };
> export default MemberInfo;
> ```
>
> 3. Lalu pada App.jsx panggil MemberInfo dengan code seperti dibawah ini:
>
> ```javascript
> import "./App.css";
> import MemberInfo from "./components/MemberInfo";
>
> function App() {
>   return (
>     <>
>       <MemberInfo
>         name={"ilham"}
>         age={"20"}
>         info={"Peserta bootcamp FrontEnd Skilvul"}
>         imgUrl="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2022/03/08055643/Cari-Dokter-Umum-Terbaik-di-Yogyakarta_-Ini-5-Rekomendasinya.jpg"
>       />
>
>       <MemberInfo
>         name={"Intan"}
>         age={"20"}
>         info={"Peserta bootcamp FrontEnd Skilvul"}
>         imgUrl="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2022/03/08055643/Cari-Dokter-Umum-Terbaik-di-Yogyakarta_-Ini-5-Rekomendasinya.jpg"
>       />
>
>       <MemberInfo
>         name={"Ujang"}
>         age={"20"}
>         info={"Peserta bootcamp FrontEnd Skilvul"}
>         imgUrl="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2022/03/08055643/Cari-Dokter-Umum-Terbaik-di-Yogyakarta_-Ini-5-Rekomendasinya.jpg"
>       />
>     </>
>   );
> }
> ```

### <b>6. State & Props</b>

> State merupakan data lokal <br>
> Props digunakan agar component memiliki data yang dinamis yang dikirim dari component lain.<br><br>
> Stateless berarti tidak memiliki state, dan hanya memiliki props. <br><br>
> Stateful berarti memiliki state dan dapat mengirim state tersebut ke component.

### Rabu, 26 Oktober 2022<br><br>

Materi : React JS State & Props <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :

- Peserta mampu memahami state dan props <br>

### <b>1. Membuat fungsi decrement dan increment pada React JS</b>

> ```javascript
> import { useState } from "react";
>
> function Counter() {
>   const [count, setCount] = useState(0); // --> useState itu isinya array [0,1,2,....dst]
>   //let count = 0     ---> ini kalo tidak menggunakan state
>   //state juga berfungsi agar isi dari variabel bisa berubah-ubah
>   const increment = () => {
>     setCount(count + 1); //benar
>     //count = count + 1 //salah karena tidak menggunakan state.
>   };
>   const decrement = () => {
>     setCount(count - 1);
>   };
>
>   return (
>     <>
>       <button onClick={decrement}> - </button>
>       <p>{count}</p>
>       <button onClick={increment}> + </button>
>     </>
>   );
> }
> export default Counter;
> ```

### <b>2. Membuat fungsi looping di react js</b>

> ```javascript
> import react from "react";
> import Card from "./Card";
>
> function ListUser(){
>   const [users, setUsers] = useState([
>       {name: "Ilham", umur: 20},
>       {name: "Intan", umur: 20},
>       {name: "Ujang", umur: 20},
>   ])
>
> return(
>   <>
>      {users.map((item, index) =>(
>       <Card key = {index} name = {item.name} umur = {item.umur} />
>      ))}
>   </>
> )
> }
> Export default ListUser
> ```

### Kamis, 27 Oktober 2022<br><br>

Materi : React JS Hooks <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :

- Apa itu Hooks ?<br>
- Perbedaan functional component dan class component <br>
- Apa useState ? <br>
- useState Syntax Structure
- Cara penggunaan useState

### <b>1. Apa itu Hooks ?</b>

> - Hooks berfungsi untuk memudahkan penggunaan functional components agar bisa menggunakan state, lifecycle, dan lainnya.
> - Sebelumnya state dan lifecycle hanya bisa digunakan di class component, namun dengan hooks, kita dapat menggunakannya di functional component.
> - Hooks yang sering digunakan adalah useState dan useEffect (mirip seperti state dan lifecycle).

### <b>2. Kelebihan penggunaan hooks</b>

> Dengan menggunakan hooks, kode jadi terlihat lebih simple, clean, dan mudah dimengerti.

### <b>3. Apa itu useState ?</b>

> Adalah sama seperti dengan state biasa, tetapi penggunaannya sedikit berbeda dengan setState/ state di class component.<br>
> Structure dari useState, seperti dibawah ini:
> ![Structure useState](https://freecontent.manning.com/wp-content/uploads/managing-component-state_04.png)

### <b>4. Cara penggunaan useState</b>

> 1. Import useState dari React
>
> ```javascript
> import { useState } from "react";
> ```
>
> 2. Menuliskan useState Hooks
>
> ```javascript
> const [nama, setName] = useState("Luthfi");
> ```
>
> 3. Pemanggilan data
>
> ```javascript
> <p>Halo, saya {nama}</p>
> ```
>
> 4. Update state
>
> ```javascript
> <button onClick={setNama("David")}> Ubah </button>
> ```

### <b>4. Array dalam useState Hooks</b>

> Kita dapat menyimpan data dalam state menggunakan array, kita tinggal menggunakan tanda [ ] dalam useState untuk menandakan
>
> ```javascript
> const [nama, setNama] = useState([]);
> ```

### <b>5. Array dalam useState Hooks</b>

> useState biasa digunakan ketika menyimpan data suatu form yang nantinya akan dipost ke API untuk di proses. <br>
> Contoh kasus lainnya ketika melakukan call API, data hasil get dapat disimpan kedalam state menggunakan useState.

### <b>6. Apa itu useEffect Hooks ?</b>

> Merupakan hooks yang bisa digunakan untuk menggunakan lifecycle pada functional component dengan mudah.

### <b>7. Apa itu lifeCycle ?</b>

> - Jika dianalogikan bisa dianggap seperti lingkaran kehidupan selama 24 jam mulai dari bangun tidur hingga tidur lagi.
> - lifeCycle yang ada didalam hooks, hanya menggunakan useEffect yang mengsatukan componentDidMount, componentDidUpdate, dan componentWillMount.

### <b>8. Penggunaan useEffect</b>

> - Penggunaan useEffect, bisa dimasukan sebelum melakukan render, useEffect sendiri biasanya sendiri biasanya ditempatkan dibawah useState.
> - Nantinya, apa yang kita tuliskan dalam useEffect akan dijalankan setiap component baru di mount (componentDidMount), terjadi perubahan (componentDidUpdate), dan pada saat component akan ditinggalkan (componentWillMount).

### <b>9. Cara penggunaan useEffect</b>

> 1. import useEffect
>
> ```javascript
> import { useEffect } from "react";
> ```
>
> 2. Tuliskan penggunaan useEffect sebelum dirender
>
> ```javascript
> useEffect(() => {
>   console.log("telah terjadi perubahan");
> }, [nama]);
> ```

### <b>10. Penggunaan useEffect Hooks</b>

> Biasa digunakan ketika membuat suatu call API, karena API akan selalu dipanggil ketika komponen terbentuk, maka call API bisa dilakukan di dalam useEffect.
