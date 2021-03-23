# JavaScript Array Methods
Array merupakan tipe data yang digunakan untuk menyimpan sekumpulan elemen dalam satu tempat. Setiap elemen dalam array memiliki nomer indeks yang berfungsi sebagai referensi untuk elemen tersebut agar dapat diakses.
<br>

Indeks pada array selalu dimulai dari angka 0, lalu diikuti dengan angka 1 dan seterusnya. untuk mengambil elemen pada array biasanya menggunakan sebuah perulangan (looping), tetapi di Javascript ada sebuah method-method yang memang dibuat khusus untuk array.
<br><br>

Baca Melalui Website : [https://febriadj.herokuapp.com/articles/penggunaan-method-method-pada-array-javascript](https://febriadj.herokuapp.com/articles/penggunaan-method-method-pada-array-javascript)

# Push, Pop, Shift, Unshift
Keempat method ini digunakan untuk menambahkan data dan mengapus data dalam array, lebih jelasnya perhatikan kode program dibawah ini.
<br>

```js
const arr = [ "yellow", "pink", "black" ]

console.log( arr.push("green") )
// [ yellow, pink, black, green ]
```
Method `push` berfungsi untuk menambahkan atau memasukkan data kedalam array pada indeks terakhir
<br><br>

```js
const arr = [ "yellow", "pink", "black" ]

console.log( arr.pop() )
// [ yellow, pink ]
```
Method `pop` berfungsi untuk menghapus data yang berada di indeks terakhir didalam array
<br><br>

```js
const arr = [ "yellow", "pink", "black" ]

console.log( arr.shift() )
// [ pink, black ]
```
Fungsi dari method `shift` adalah kebalikan dari method `pop`, yaitu menghapus data yang berada di indeks paling awal didalam array
<br><br>

```js
const arr = [ "yellow", "pink", "black" ]

console.log( arr.unshift("blue") )
// [ blue, yellow, pink, black ]
```
Fungsi dari method `unshift` adalah kebalikan dari method `push`, yaitu menambah atau memasukkan data ke indeks paling awal didalam array.

# Map, Find, Filter, Reduce
Selanjutnya adalah method map, find, filter dan reduce, keempat method ini masing-masing memiliki kegunaan yang berbeda-beda.
<br>

Untuk mencoba keempat method ini ada baiknya untuk membuat struktur array yang lebih kompleks lagi dari sebelumnya.
<br><br>

```js
const books = [
  { title: 'learn reactjs', item: 2 },
  { title: 'basic javascript', item: 5 }
  { title: 'mern stack', item: 3 }
]
```
Sekarang variabel `books` sudah dibuat yang berisikan 3 elemen berbentuk objek, lalu disetiap objek tersebut memiliki key dan valuenya masing-masing.
<br><br>

```js
books.map( res => console.log(res) )

/*
{ title: 'learn reactjs', item: 2 },
{ title: 'basic javascript', item: 5 }
{ title: 'mern stack', item: 3 } 
*/
```
Kegunaan method `map` ini sama seperti `foreach` yaitu menampilkan semua elemen atau data didalam array tersebut secara berurutan.
<br><br>

```js
const x = books.find( e => e.title == 'mern stack' )

console.log(x)
// { title: 'mern stack', item: 3 }
```
Method `find` digunakan untuk menampilkan elemen yang terkait dengan kondisi. Method ini hanya menampilkan 1 buah elemen saja. Pada kode program diatas, penulis ingin menampilkan elemen yang mempunyai `title` berisikan 'mern stack'.
<br><br>

```js
const x = books.filter( e => e.item < 5 )

console.log(x)
/*
[
  { title: 'learn reactjs', item: 2 }
  { title: 'mern stack', item: 3 }
]
*/
```
Sederhananya fungsi dari method `filter` ini seperti memfilter atau menyaring, method ini hanya akan menampilkan elemen yang sesuai dengan kondisinya. pada kode program diatas, jumlah item yang lebih besar sama dengan 5 tidak akan ikut ditampilkan.
<br><br>

Selanjutnya method `reduce`, agar dapat mengetahui lebih jelas lagi cara kerja method  `reduce` ini, gunakan struktur array baru yang lebih sederhana yang hanya berisikan angka.
<br>

```js
const num = [ 3, 5, 9, 4 ]
const x = num.reduce( (acc, cur) => acc + cur )

console.log(x)
// 21
```
Method `reduce` akan menjumlahkan setiap elemen atau nilai didalam array, berawal dari kiri lalu kekanan.
Bisa dilihat pada program diatas, kenapa outputnya bisa 21? coba perhatikan baik-baik lalu jumlahkan semua nilai yang ada didalam array num tersebut. 3 + 5 = 8; 8 + 9 = 17; 17 + 4 = 21. 

# Method Lainnya
Selain method-method yang sudah dijelaskan diatas, masih banyak method yang dapat digunakan untuk bekerja dengan array.
<br><br>

```js
const arr = [ "white", "black", "yellow" ]

arr.forEach( res => console.log(res) )
// white, black, yellow
```
Pada artikel ini sudah dijelaskan diatas dari kegunaan dari method `forEach`, fungsi method ini sama seperti `map` yaitu untuk menampilkan seluruh elemen didalam array secara berurutan
<br><br>

```js
const arr = [ "white", "black", "yellow" ]

console.log( arr.reverse() )
// [ yellow, black, white ]
```
Sesuai dengan arti dari namanya `reverse` yaitu membalikkan, method ini berfungsi untuk menampilkan seluruh elemen secara berurutan dimulai dari indeks terakhir.
<br><br>

```js
const arr = [ 4, 6, 8, 2 ]

console.log( arr.sort() )
// [ 2, 4, 6, 8 ]
```
Method `sort` ini berfungsi untuk menampilkan seluruh elemen secara berurutan dimulai dari nilai yang terkecil dan disimpan didalam objek array baru.
<br><br>

```js
const arr = [ "apple", "banana", "melon" ]

console.log( arr.indexOf("melon") )
console.log( arr.findIndex( e => e == "melon" )
// 2
```
Kedua Method ini `indexOf` dan `findIndex` mempunyai fungsi yang sama dan cukup sederhana, yaitu menampilkan indeks dari nilai yang dicari
<br><br>

```js
const arr = [ 2, 7, 4, 3, 9 ]

console.log( arr.some( e => e < 5 ) )
// true

console.log( arr.every( e => e < 5 ) )
// false
```
Output dari method `some` dan `every` ini sama yaitu hanya berupa true atau false saja (boolean), tetapi cara kerja dari kedua method ini berbeda.
<br>

Untuk method `some` jika ada salah satu nilai saja didalam array yang sesuai dengan kondisi, maka akan menghasilkan true.
<br>

Lalu untuk method `every` semua nilai harus sesuai dengan kondisi, jika ada salah satu saja yang tidak sesuai, maka akan menghasilkan false.
<br><br>

```js
const str = [ "js", "ruby", "go" ]
const int = [ 1, 2, 3 ]

console.log( str.concat(int) )
// [ js, ruby, go, 1, 2, 3 ]
```
Method `concat` berfungsi untuk menggabungkan atau menyatukan 2 atau lebih array kedalam satu objek array baru.
<br><br>

```js
const arr = [ "a", "b", "c", "d", "e" ]

console.log( arr.slice(2, 4) )
// [ c, d ]
```
Method `slice` ini nantinya akan membuat sebuah objeks array baru, method ini mempunyai 2 parameter, parameter pertama untuk menentukan nomer indeks elemen awal yang akan dieksekusi dan paramater kedua untuk menentukan akhir indeks elemen
<br><br>

```js
const arr = [ "f", "e", "b" , "r", "i" ]

console.log(arr.join(""))
// febri

console.log(arr.join("-"))
// f-e-b-r-i
```
Terakhir adalah method `join`, method ini berfungsi untuk mengubah array menjadi string, dengan `join` array akan disatukan dengan karakter penghubung.
<br>

Kegunaan method `join` ini kurang lebih sama dengan method `toString` dan `toLocaleString`, hanya saja method `join` ini lebih flexible dalam penggunaannya.