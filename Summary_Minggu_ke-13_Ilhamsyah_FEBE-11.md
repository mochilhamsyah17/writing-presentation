# Summary <br> Kelas Web Development Basic

### MSIB Skilvul Minggu ke-13

<hr>

Materi : React Context & Testing <br> Mentor : Kak Auzan Assidqi <br>
Objective Learnings :

-  Peserta mampu memahami dan menggunakan React Context untuk State Management
- Peserta mampu memahami Unit Testing
- Peserta mampu membuat Unit testing dengan Jest
- Peserta mampu membuat mocking dan handle asynchronous testing dengan Jest
- Peserta mampu membuat testing untuk component React.js menggunakan RTL


<br>

## <b>React Context</b>
### <B>1. Apa itu Context ?</b>

> React Context menyediakan cara untuk oper data melalui diagram komponen tanpa harus oper props secara manual di setiap tingkat. <br>
> React Context dapat diinstall dengan menggunakan: 
> ```js
> npm install react-context --save
> ```
> Context dirancang untuk berbagi data yang dapat dianggap “global” untuk diagram komponen React, seperti pengguna terotentikasi saat ini, tema, atau bahasa yang disukai. Misalnya, dalam kode di bawah ini kita secara manual memasang prop “theme” untuk memberi style pada komponen Button:
> ```js
> class App extends React.Component {
>   render() {
>     return <Toolbar theme="dark" />;
>   }
> }
> 
> function Toolbar(props) {
>   // komponen Toolbar harus menggunakan *prop* "theme" tambahan
>   // dan oper ke ThemedButton. Ini bisa menjadi *painful*
>   // jika setiap tombol di dalam aplikasi perlu mengetahui *theme*-nya
>   // karena itu harus melewati semua komponen.
>   return (
>     <div>
>       <ThemedButton theme={props.theme} />
>     </div>
>   );
> }
> 
> class ThemedButton extends React.Component {
>   render() {
>     return <Button theme={this.props.theme} />;
>   }
> }
> ```
> Menggunakan context, kita dapat menghindari mengoper props melalui elemen perantara:
> ```js
> // Context memungkinkan kita untuk oper nilai ke dalam diagram komponen
> // tanpa secara ekplisit memasukannya ke dalam setiap komponen.
> // Buat *context* untuk tema saat ini (dengan "light" sebagai default).
> const ThemeContext = React.createContext('light');
> 
> class App extends React.Component {
>   render() {
>     // Gunakan Provider untuk oper tema saat ini ke diagram di bawah ini.
>     // Komponen apa pun dapat membacanya, tidak peduli seberapa dalam diagram tersebut.
>     // Dalam contoh ini, kita mengoper "dark" sebagai nilai saat ini.
>     return (
>       <ThemeContext.Provider value="dark">
>         <Toolbar />
>       </ThemeContext.Provider>
>     );
>   }
> }
> 
> // Komponen di tengah tidak harus 
> // oper temanya secara ekplisit lagi.
> function Toolbar() {
>   return (
>     <div>
>       <ThemedButton />
>     </div>
>   );
> }
> 
> class ThemedButton extends React.Component {
>   // Tetapkan contextType untuk membaca *context theme* saat ini.
>   // React akan menemukan Provider *theme* terdekat di atas dan menggunakan nilainya.
>   // Dalam contoh ini, *theme* saat ini adalah "dark".
>   static contextType = ThemeContext;
>   render() {
>     return <Button theme={this.context} />;
>   }
> }
> ```

### <B>2. API pada React Context ?</b>

> - <b>React.createContext</b>
> ```js
> const MyContext = React.createContext(defaultValue);
> ```
> Buat objek Context. Ketika React render komponen yang menerima objek Context ini akan membaca nilai context saat ini dari pencocokan terdekat Provider di atasnya dalam diagram. <br>
> Argumen defaultValue hanya digunakan ketika komponen tidak memiliki Provider yang cocok di atasnya dalam diagram. Ini dapat membantu untuk testing komponen secara terpisah tanpa membungkusnya. Catatan: mengoper undefined sebagai nilai Provider tidak menyebabkan konsumsi komponen menggunakan defaultValue. <br>
> - <b>Context.Provider</b>
> ```js
> <MyContext.Provider value={/* beberapa nilai */}>
> ```
> Menerima prop value untuk dioper ke komponen konsumsi yang merupakan keturunan Provider ini. Satu Provider dapat dihubungkan ke banyak consumer. Provider dapat disarangkan untuk override nilai lebih dalam di dalam diagram. <br>
> Semua consumer yang merupakan keturunan Provider akan render ulang setiap kali prop value dalam Provider berubah. Perambatan dari Provider ke consumer turunannya (termasuk .contextType dan useContext) tidak tunduk ke method shouldComponentUpdate, sehingga consumer diperbarui bahkan ketika komponen leluhur menebus pembaruan tersebut. <br>
Perubahan ditentukan dengan membandingkan nilai-nilai baru dan lama menggunakan algoritma yang sama dengan Object.is. <br>
> - <b>Class.contextType</b>
> ```js
> class MyClass extends React.Component {
>   componentDidMount() {
>     let value = this.context;
>     /* melakukan efek samping saat *mount* menggunakan nilai MyContext */
>   }
>   componentDidUpdate() {
>     let value = this.context;
>     /* ... */
>   }
>   componentWillUnmount() {
>     let value = this.context;
>     /* ... */
>   }
>   render() {
>     let value = this.context;
>     /* *render* sesuatu berdasarkan nilai dari MyContext */
>   }
> }
> MyClass.contextType = MyContext;
> ```
> Properti contextType pada kelas dapat diberikan objek Context yang dibuat oleh React.createContext(). Ini memungkinkan Anda menggunakan nilai saat ini terdekat dari tipe Context menggunakan this.context. Anda dapat merujuk ini dalam salah satu method lifecycle termasuk fungsi render. <br>
> - <b>Context.Consumer</b>
> ```js
> <MyContext.Consumer>
>   {value => /* render sesuatu berdasarkan nilai *context*-nya */}
> </MyContext.Consumer>
> ```
> Komponen React yang menerima perubahan context. Ini memungkinkan Anda menerima context di dalam komponen fungsi. <br>
> Dibutuhkan sebuah fungsi sebagai child. Fungsi menerima nilai context saat ini dan mengembalikkan node React. Argumen value yang diteruskan ke fungsi akan sama dengan prop value dari Provider terdekat untuk context ini di atas dalam diagram. Jika tidak ada Provider untuk context ini di atas, argumen value akan sama dengan defaultValue yang diteruskan ke createContext(). <br>
> - <b>Context.displayName</b>
> Objek Context menerima properti string displayName. React DevTools menggunakan string ini untuk menentukan apa yang harus di tampilkan untuk context tersebut. <br>
> Misalnya, komponen berikut ini akan muncul sebagai MyDisplayName di DevTools:
> ```js
> const MyContext = React.createContext(/* beberapa nilai */);
> MyContext.displayName = 'MyDisplayName';
> 
> <MyContext.Provider> // "MyDisplayName.Provider" in DevTools
> <MyContext.Consumer> // "MyDisplayName.Consumer" in DevTools
> ```

### <b>PERINGATAN</b>
> Karena context menggunakan identitas referensi untuk menentukan kapan harus render ulang, ada beberapa gotcha yang dapat memicu render yang tidak disengaja dalam consumer ketika parent provider render ulang. Misalnya kode di bawah ini akan render ulang semua consumer setiap kali Provider render ulang karena objek baru selalu dibuat untuk value:
> ```js
> class App extends React.Component {
>   render() {
>     return (
>       <MyContext.Provider value={{something: 'something'}}>
>         <Toolbar />
>       </MyContext.Provider>
>     );
>   }
> }
> ```
> Untuk menyiasatinya, angkat nilai ke dalam state induk:
> ```js
> class App extends React.Component {
>   constructor(props) {
>     super(props);
>     this.state = {
>       value: {something: 'something'},
>     };
>   }
> 
>   render() {
>     return (
>       <Provider value={this.state.value}>
>         <Toolbar />
>       </Provider>
>     );
>   }
> }
> ```

## <b>React Testing</b>

### <b>Apa itu react testing</b>
> React Testing Library adalah seperangkat helpers yang memungkinkan Anda mengetes komponen pada React tanpa bergantung pada detail implementasinya. Pendekatan ini membuat refactoring menjadi mudah dan juga mendorong Anda untuk menerapkan best practices untuk aksesbilitas. <br>
> Kita dapat menginstall react testing library dengan menggunakan:
> - npm
> ```js
> npm install --save-dev @testing-library/react
> ```
> - yarn
> ```js
> yarn add --dev @testing-library/react
> ```
> Testing dibagi menjadi 3 kategori, yaitu</b>
> - Unit Testing
> - Integration Testing
> - UI Testing

### <b>Apa itu Jest</b>
> Jest merupakan Javascript test runner yang berisi library javascript untuk membuat, menjalankan, dan melalkukan test structure (structuring tests) <br><br>
> Pada saat melakukan testing, terdapat 2 skenario utama. Yaitu:
> - you inherit legacy code which comes without tests
> - you have to implement a new functionality out of thin air
<br><br>

> Pada melakukan testing terdapat alur test, antara lain:
> - import the function to test
> - give an input to the function
> - define what to expect as the output
> - check if the function produces the expected output

### <b>Bagaimana cara install jest untuk react testing ?</b>

> 1. Buat folder dan inisialisasi project
> ```js
> mkdir getting-started-with-jest && cd $_
> npm init -y
> ```
> 2. Install jest dengan cara:
> ```js
> npm i jest --save-dev
> ```

### <b>Snapshot Testing with Mocks, Enzyme and React 16+</b>
> There's a caveat around snapshot testing when using Enzyme and React 16+. If you mock out a module using the following style:
> ```js
> jest.mock('../SomeDirectory/SomeComponent', () => 'SomeComponent');
> ```
> Then you will see warnings in the console:
> ```js
> Warning: <SomeComponent /> is using uppercase HTML. Always use lowercase HTML tags in React.
> 
> # Or:
> Warning: The tag <SomeComponent> is unrecognized in this browser. If you meant to render a React component, start its name with an uppercase letter.
> ```
> React 16 triggers these warnings due to how it checks element types, and the mocked module fails these checks. Your options are:
> 1. Render as text. This way you won't see the props passed to the mock component in the snapshot, but it's straightforward:
> ```js
> jest.mock('./SomeComponent', () => () => 'SomeComponent');
> ```
> 2. Render as a custom element. DOM "custom elements" aren't checked for anything and shouldn't fire warnings. They are lowercase and have a dash in the name.
> ```js
> jest.mock('./Widget', () => () => <mock-widget />);
> ```
> 3. Use react-test-renderer. The test renderer doesn't care about element types and will happily accept e.g. SomeComponent. You could check snapshots using the test renderer, and check component behavior separately using Enzyme.
> 4. Disable warnings all together (should be done in your jest setup file):
> ```js
> jest.mock('fbjs/lib/warning', () => require('fbjs/lib/emptyFunction'));
> ```