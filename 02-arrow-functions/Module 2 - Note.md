# Arrow Function

Penggunaan arrow function membuat penulisan lebih ringkas, cukup mengganti _function_ dengan tanda panah

{% codeblock %}
const fullNames = names.map(function(name){
        return `${name} armariena`;
    });

// Arrow Function
const fullNames2 = names.map((name) => {
        return `${name} armariena`;
    });
{% endcodeblock %}

Arrow function **selalu anonymous function.** Mungkin sedikit sulit untuk traceback jika ada error dikemudian hari, tapi arrow function bisa ditampung dalam variable.