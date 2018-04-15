# Arrow Function

Penggunaan arrow function membuat penulisan lebih ringkas, cukup mengganti _function_ dengan tanda panah.

```javascript
const fullNames = names.map(function(name){
        return `${name} armariena`;
    });

// Arrow Function
const fullNames2 = names.map((name) => {
        return `${name} armariena`;
    });
```

Arrow function **selalu anonymous function atau tanpa nama.** Mungkin sedikit sulit untuk traceback jika ada error dikemudian hari, tapi arrow function bisa ditampung dalam variable.

Jika argument dalam function hanya satu, tanda kurung () bisa dihilangkan. Jika argument lebih dari 1 atau kosong, harus menggunakan tanda kurung ().

```javascript
const old = ages.filter(age => age>=60); // function mengembalikan nilai dari age >= 60

const win = winners.map( (winner,i) => ({name:winner, race, place:i+1}) ); // function mengembalikan object
```

**Explicit & Implicit return**

Explicit artinya ditulis perintah return, sedangkan implicit artinya tidak perlu ditulis perintah return.
```javascript
const old = ages.filter(age => {
    return age>=60;
}); // explicit return
const old = ages.filter(age => age>=60); // implicit return
```

## this dalam Arrow Function
this dalam arrow function selalu **inherit dari paret scope.**
```javascript
const box = document.querySelector('.box');
    box.addEventListener('click', function(){
      this.classList.toggle('opening');      
});
```
Contoh diatas tidak bisa menggunakan arrow function, karena this akan inherit dari parentnya, yaitu window.

```javascript
const box = document.querySelector('.box');
box.addEventListener('click', function(){
    this.classList.toggle('opening');
    setTimeout(() => {
        this.classList.toggle('open');
    }, 500);
});
```
Pada function setTimeout, kita bisa menggunakan arrow function karena this pada setTimeout function tersebut inherit this pada parent scopenya, yaitu box.addEventListener

# Switch Value
Untuk mengganti value dari dua variable pada ES6, cukup dengan syntax sebagai berikut:
```javascript
[val1, val2] = [val2, val1];
```

# Function Default Argument
```javascript
function calculateBill(total, tax = 0.13, tip = 0.15){
    return total + (total * tax) + (total * tip);
}

const totalBill = calculateBill(100, undefined, 0.25);
```
Jika parameter tidak sama dengan argument, kita bisa memberi nilai default pada parameternya.