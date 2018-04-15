# Var, Let dan Const

## Var
var bisa **diupdate atau dideklarasi ulang.**
```javascript
var nilai = 100;
var nilai = 200;
```

var adalah **function scope.**
```javascript
function setWidth(){
    var width = 100;
    console.log(width);           
}
```

Variable width adalah temporary variable yang bisa dipakai oleh fungsi setWidth()
```javascript
var age = 100;
if (age>12) {
    var dogYears = age * 7;
    console.log(`You are ${dogYears} dog years old!`);
}
dogYears
```
Variable dogYears dibuat hanya untuk perbandingan, akan tetapi masih bisa diakses karena tidak berada dalam fungsi sehingga var dogYears berada di scope keseluruhan window.

## Let dan Const
Let dan const adalah **block scope.**
Let menggantikan var, bisa diupdate akan tetapi tidak bisa dideklarasi ulang dalam satu scope.
Const hanya bisa dideklarasi satu kali dan tidak bisa diupdate.