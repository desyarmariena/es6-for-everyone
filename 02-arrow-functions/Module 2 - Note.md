# Arrow Function

Penggunaan arrow function membuat penulisan lebih ringkas, cukup mengganti _function_ dengan tanda panah

```javascript
const fullNames = names.map(function(name){
        return `${name} armariena`;
    });

// Arrow Function
const fullNames2 = names.map((name) => {
        return `${name} armariena`;
    });
```

Arrow function **selalu anonymous function.** Mungkin sedikit sulit untuk traceback jika ada error dikemudian hari, tapi arrow function bisa ditampung dalam variable.

Jika parameter dalam function hanya satu, tanda kurung () bisa dihilangkan. Jika parameter lebih dari 1 atau kosong, harus menggunakan tanda kurung ().

```javascript
const old = ages.filter(age => age>=60); // function mengembalikan nilai dari array >= 60

const win = winners.map( (winner,i) => ({name:winner, race, place:i+1}) ); // function mengembalikan object
```

**Explicit & Implicit return**
Explicit artinya ditulis perintah return, sedangkan implicit artinya tidak perlu ditulis perintah return.
```javascript
const old = ages.filter(age => {
    return age>=60;
}); // explicit return
const old = ages.filter(age => age>=60); // explicit return
```