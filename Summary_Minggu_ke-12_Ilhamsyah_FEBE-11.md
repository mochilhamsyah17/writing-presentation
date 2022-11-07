# Summary <br> Kelas Web Development Basic

### MSIB Skilvul Minggu ke-12

<hr>

Materi : Intro React JS and Installation <br> Mentor : Kak Dila, Kak Auzan Assidqi <br>
Objective Learnings :

- Peserta mampu memahami dan menggunakan PropTypes
- Peserta mampu memahami konsep routing pada React.js
- Peserta mampu membuat routing dasar
- Peserta mampu membuat dynamic route 
- Peserta mampu membuat nested route
- Peserta mampu memahami konsep dan menggunakan Redux
- Peserta mampu memahami dan menggunakan React Redux
- Peserta mampu memahami dan menggunakan Redux Thunk

<br>

## <b>Prop types</b>
### <B>1. Apa itu Proptypes ?</b>

> PropTypes merupakan library untuk menvalidasi props. Ini sangat membantu dalam meminimalkan bugs saat mengembangkan App besar. Jika props tidak benar type nya maka akan muncul warning atau pesan error.<br>

### <b>2. Bagaimana cara install Proptypes ?</b>

> Proptypes dapat diinstall dengan menggunakan :
> ```bash
> npm install prop-types
> ```
> <br>

### <b>3. Contoh penggunaan Proptypes</b>

> - Proptypes dapat diimport menggunakan :
> ```javascript
> import PropTypes from 'prop-types';
> ```
> - Penentuan type data props dapat menggunakan seperti dibawah ini:
> ```javascript
> Header.propTypes = {
>    name: PropTypes.string,
>    age: PropTypes.number, 
>    data: PropTypes.array,
>   };
> ```

### <b>4. Memberikan opsi tipe data menggunakan PropTypes</b>
> - Pada Proptypes kita dapat membuat opsi pada sebuah variabel untuk dapat menampung tipe data yang telah ditentukanm, dengan cara seperti dibawah ini:
> ```javascript
> age: PropTypes.oneOfType([PropTypes.number, Proptypes.string])
> ```

### <b>5. Mengecek nilai dari object</b>
> ```javascript
> info: PropTypes.shape({
>     hobby: PropTypes.string,
>     class: PropTypes.number,
>   })
> ```

### <b>6. Mengecek nilai dari key object</b>
> ```javascript
> info: PropTypes.exact({
>    hobby: PropTypes.string,
>    class: PropTypes.number,
>  }).isRequired,
> ```

<br>

## <b>React Router</b>

### <b>1. Apa itu react router ?</b>
> React Router adalah sistem perpustakaan standar yang dibangun di atas React dan digunakan untuk membuat perutean di aplikasi React menggunakan Paket React Router. Ini menyediakan URL sinkron di browser dengan data yang akan ditampilkan di halaman web. Ini memelihara struktur standar dan perilaku aplikasi dan terutama digunakan untuk mengembangkan aplikasi web satu halaman.

### <b>2. Bagaimana cara menginstall react router ?</b>
> Kita dapat menginstall react router dengan syntax dibawah ini:
> ```javascript
> npm install react-router-dom@6
> ```

### <b>3. Bagaiamana cara menggunakan react router ?</b>
> - Import dulu routernya dengan menggunakan 
> ```JS
> import { BrowserRouter } from "react-router-dom";
> ``` 
> - Kita dapat menggunakan react router dengan menggunakan ``<BrowserRouter></BrowserRouter>`` yang mana file yang ingin menggunakan routing maka perlu disisipkan pada tag BrowserRouter, contohnya:
> ```JS
> <BrowserRouter>
>   <fileUtama />
> </BrowserRouter>
> ```
> - import Routes, Route, Link
> ```JS
> import { Routes, Route, Link } from "react-router-dom";
> ```
> - Route Parameter
> ```JS
> <Route path="/detail/:id" element={<DetailPage />} />
> ```
> - Penggunaan Nested route
> ```JS
>   <Route path="/about" element={<AboutPage />}>
>       <Route path="student" element={<AboutStudent />} />
>       <Route path="teacher" element={<AboutTeacher />} />
>       <Route index element={<AboutSchool />} />
>   </Route>
> ```
> - Routes berfungsi untuk menampung satu atau banyak dari route.
> ```JS
> <Routes> 
>   <Route path="/about" element={<AboutPage />}>
>       <Route path="student" element={<AboutStudent />} />
>       <Route path="teacher" element={<AboutTeacher />} />
>       <Route index element={<AboutSchool />} />
>   </Route>
> </Routes>
> ```
> - index digunakan agar element AboutSchool langsung ditampilkan pertama kali ketika page about dibuka
> ```JS
> <Route index element={<AboutSchool />} />
> ```
> - Penggunaan Link sama seperti penggunaan tag anchor pada html. untuk href="" diganti dengan to={} untuk menuju ke alamat page yang diinginkan
> ```JS
> <nav>
>   <Link to={"/"}>Home |</Link>
>   <Link to={"/about"}>About</Link>
> </nav>
> ```
> - tambahkan path="*" untuk menampilkan halaman yg tidak ditemukan. case nya adalah ketika user mengakses path tertentu yang tidak terdaftar di routingan yang kita miliki
> ```JS
> <Route path="*" element={<NotFound />} />
> ```
<br>

## <b>React Redux</b>

### <b>1. Apa itu redux ?</b>
> Redux adalah salah satu state management yang sangat hype pada waktunya dan masih relevan sampai sekarang. <br>
> Eedux didukung package middleware yang bertebaran di npm yang mana memudahkan kita untuk melakukan development seperti redux-thunk, redux-saga, redux-persist dan sebagainya. 
> <br>Kalau kita memilih context API dibanding redux bisa-bisa saja tapi untuk logic seperti thunk nanti kita butuh melakukan extra karena harus buat dari scratch.

### <b>2. Bagaimana cara menggunakan redux ?</b>
> - React redux dapat diinstall menggunakan :
> ```JS
> npm install redux react-redux
> ```
> - Siapkan folder redux di dalam src/
> - Lalu pada folder src/redux/ kita buat file store.js yang berisikan
> ```javascript
> import { createStore } from 'redux'
> import keranjangReducer from '../reducer/keranjangReducer'
> 
> const store = createStore(keranjangReducer)
> 
> export default store
> ```
> - <b>Store</b> berfungsi untuk menggabungkan Action dan Reducer agar bisa bekerja sebagai state manajemen.
> - Buat folder baru actions di dalam folder redux [/src/redux/actions/] dan buat sebuah file bernama keranjangReducer.js yang berisikan:
> ```js
> export const INCREMENT_KERANJANG = "INCREMENT_KERANJANG"
> export const DECREMENT_KERANJANG = "DECREMENT_KERANJANG"
> 
> export function incrementKeranjang() {
>   console.log("action dipanggil")
>   return {
>     type: INCREMENT_KERANJANG
>   }
> }
> 
> export function decrementKeranjang() {
>   return {
>     type: DECREMENT_KERANJANG
>   }
> }
> ```
> - <b>Action</b> bisa menampung data dengan cara menambahkan property kedua dalam object Action-nya.
> - Lalu selanjutnya ada <b>Reducer</b>, Reducer adalah bagian redux yang merubah state menjadi respon yang terjadi ketika Action di dispatch() .
> - Untuk merubah state hanya bisa dilakukan di Reducer, dan Reducer hanya melakukan perubahan state jika ada action yang di dispatch() . Secara sederhana reducer ini hanya sebuah function yang mengembalikan state baru.
> - Lalu kita buat file keranjangReducer pada folder reducer yang berisikan :
> ```js
> import {
>   INCREMENT_KERANJANG,
>   DECREMENT_KERANJANG,
> } from "../action/keranjangAction";
> 
> const initialState = {
>   totalKeranjang: 0,
> };
> 
> function keranjangReducer(state = initialState, action) {
>   console.log(action);
> 
>   switch (action.type) {
>     case INCREMENT_KERANJANG: 
>       return {
>         totalKeranjang: state.totalKeranjang + 1
>       }
>     case DECREMENT_KERANJANG: 
>       return {
>         totalKeranjang: state.totalKeranjang - 1
>       } 
>     default:
>       return state;
>   }
> }
> 
> export default keranjangReducer;
> ```

### <b>Provider</b>
> Provider adalah component yang disediakan oleh library react-redux yang telah kita install sebelumnya. Component provider memiliki props berupa store (redux store). Component provider akan membungkus semua component yang ada sehingga semua component tersebut dapat mengakses informasi yang ada pada redux store. Contoh penggunaan Provider ada dibawah ini:
> ```js
> <Provider store={store}>
>      <Router>
>      <div className="App">
>        <Layout>
>          <div className="content">
>            <Switch>
>              <Route path="/masuk">
>                <Login />
>              </Route>
>              ...
>              <Route exact path="/">
>                <Home />
>              </Route>
>            </Switch>
>          </div>
>        </Layout>
>        </div>
>      </Router>
> </Provider>
> ```

## <b>Hooks</b>
> <b>useSelector()</b>
> <br> merupakan mirip dengan mapState ke props. useSelector akan dipanggil dengan seluruh Redux store state sebagai satu-satunya argumen. useSelector() juga akan berlangganan ke Redux state, dan menjalankan pemilih setiap kali tindakan dikirim. <br>
> <b>Perbedaan useSelector dengan mapState :</b>
> 1. When an action is dispatched, useSelector() will do a reference comparison of the previous selector result value and the current result value. If they are different, the component will be forced to re-render. If they are the same, the component will not re-render.
> 2. useSelector() uses strict === reference equality checks by default, not shallow equality (see the following section for more details).
> 3. The selector function does not receive an ownProps argument. However, props can be used through closure (see the examples below) or by using a curried selector.<br>

Contoh penggunaan useSelector:
> ```js
> import React from 'react'
> import { useSelector } from 'react-redux'
> 
> export const CounterComponent = () => {
>   const counter = useSelector((state) => state.counter)
>   return <div>{counter}</div>
> }
> ```

> <b>useDispatch()</b>
> <br>Hook yang satu ini mengembalikan reference ke fungsi pengiriman dari Redux Store. Kita dapat mengirim action menggunakan ini<br>
> Contoh penggunaan useDispatch:
> ```js
> import React from 'react'
> import { useDispatch } from 'react-redux'
> 
> export const CounterComponent = ({ value }) => {
>   const dispatch = useDispatch()
> 
>   return (
>     <div>
>       <span>{value}</span>
>       <button onClick={() => dispatch({ type: 'increment-counter' })}>
>         Increment counter
>       </button>
>     </div>
>   )
> }
> ```

> <b>useStore()</b><br>
> Berbeda dengan useDispatch, useStore mengembalikan referensi ke Redux Store yang sama yang diteruskan ke komponen ``<provider>``
> <br>Berikut contoh penggunaannya:
> ```js
> import React from 'react'
> import { useStore } from 'react-redux'
> 
> export const CounterComponent = ({ value }) => {
>   const store = useStore()
> 
>   return <div>{store.getState()}</div>
> }
> ```

## <b>THUNK</b>

### <b> Pengertian Thunk</b>
> Thunk merupakan fungsi redux yang secara spesifik berisikan logic asynchronus. Thunks ditulis dengan 2 fungsi yaitu:
> - Dalam function thunk, terdapat dispatch dan getState argumen
> - diluar pembuatan function, yang mana membuat dan mengembalikan function thunk.

### <b> Cara install react redux thunk</b>
> ```js
> npm install redux-thunk
> ```

## <b>Cara enable redux thunk</b>
> Redux Thunk dapat digunakan menggunakan ``applyMiddlaware()``
> ```js
> import { createStore, applyMiddleware } from 'redux'
> import thunk from 'redux-thunk'
> import rootReducer from './reducers/index'
> 
> const store = createStore(rootReducer, applyMiddleware(thunk))
> ```

### <b>Contoh penggunaan thunk pada counterSlice</b>
> ```js
> // The function below is called a thunk and allows us to perform async logic.
> // It can be dispatched like a regular action: `dispatch(incrementAsync(10))`.
> // This will call the thunk with the `dispatch` function as the first argument.
> // Async code can then be executed and other actions can be dispatched
> export const incrementAsync = amount => dispatch => {
>   setTimeout(() => {
>     dispatch(incrementByAmount(amount))
>   }, 1000)
> }
> ```
> Atau kita juga dapat menggunakan dengan cara redux action seperti biasanya:
> ```js
> store.dispatch(incrementAsync(5))
> ```
