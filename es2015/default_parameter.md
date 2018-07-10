### Default Parameter

Pada javascript parameter dari sebuah fungsi secara default akan bernilain **undefined**.
Oleh karena itu pada keadaan tertentu kita harus memeriksa apakah nilai dari parameter sebuah fungsi telah diberikan atau belum, jika belum maka kita berikan nilai default kepada parameter tersebut.  
Jika tidak memberikan nilai default pada parameter, maka kemungkinan code kita bisa menjadi error karena parameter yang belum diberikan nilai akan bernilai **undefined**.

Berikut adalah contoh bagaimana cara untuk memeriksa lalu memberikan nilai dari sebuah parameter :

```javascript
// es5
function contoh(a, b) {
  // cara memeriksa lalu memberikan nilai default pada parameter
  b = typeof b !== "undefined" ? b : 2;

  console.log(a);
  console.log(b);
}

// panggil fungsi diatas
contoh();
```

maka jika fungsi diatas di jalankan, outputnya adalah :

```
undefined
2
```

Pada contoh diatas, hanya untuk memberikan nilai default pada parameter kita perlu melakukan beberapa langkah.  
Eits, tenang.. di es2015 hal tersebut di optimasi lagi agar lebih efisien dan mudah untuk memberikan nilai default kepada parameter.

Dibawah ini adalah code yang sama, yg ditulis dengan es2015 untuk memberikan nilai **default parameter** dan menghasilkan output yang sama.

```javascript
// es2015
function contoh(a, b = 2) {
  console.log(a);
  console.log(b);
}

// panggil fungsi diatas
contoh();
```

Penulisan dengan es2015 jauh lebih efisien dan simple.  
Pada kedua contoh diatas, parameter **a** bernilai **undefined** dan **b** bernilai **2** walaupun pada pemanggilan fungsi **contoh** kita tidak memberikan nilai apapun kepada kedua parameternya.

Mari kita lihat contoh lainnya :

```javascript
function nama(awal, akhir = "(nino)") {
  return awal + akhir;
}

console.log(nama("hermawan ", "ganteng"));
```

Maka output yang dihasilkan :

```
hermawan ganteng
```

Jika diperhatikan bahwa ketika memanggil fungsi **nama**, kita memberikan nilai untuk parameter **awal** dan **akhir**.
Namun nilai default dari parameter akhir akan digantikan dengan nilai baru yang telah kita berikan.
Dalam artian nilai **default parameter** hanya akan digunakan jika tidak nilai parameter yang diberikan saaat pemanggilan fungsi.
