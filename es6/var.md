# Bueno, hablemos de var  en javascript con unos ejemplitos para ser breves


1. Veamos si inicializando una variable dentro de una funcion instancia su memoria

```js
function inicializarVar() {
  var inicial = 0;
}

inicializarVar();
console.log(inicial) // Se caera 
// Asi que cuando lo inicializamos importa

```

2. A ver si dentro de una funcion podemos tomar variables de por fuera con el mismo nombre

```js

// Hacemos una inicializacion aqui
var hola = '9'
function saludar() {
  // Pero aqui no existe
  console.log('hola', hola)
  // Aqui tampoco
  hola++;
  console.log('hola2', hola)
  // Aqui reinicializamos la variable cambia la que creamos afuera ?
  var hola = 2;
  console.log('hola3', hola)
  // Aqui cambia la variable que reinicializamos
  hola--;
  console.log('hola4', hola)
}
```


3. Que onda con las variables que dicen aveces undefined y aveces se caen

```js
var a = 2

function saludar() {
  console.log('b', b) // Que diga que es undefined esta bien
  // Ya separo su espacio en memoria
  console.log('c' , chau) // Chau se caera, porque ? porque no lo declaramos asi que no tiene una referencia 
  // a esta variable

  b = b + 2;
  console.log('b', b)
  
  var b = '2323'
  console.log('b', b)
}

```


4. veamos el llamar a variables que nunca defino denttro de una funcion


```js

var ejecutado = 'yep';

function ejecutar() {
  console.log('ejecutado', ejecutado) // si funciona 

  console.log(hola)
  var hola = 'holaaaaaa';
  console.log(hola)

  // var ejecutado = 'holi' // si agrego esta linea sale undefined porque ya reservo espacio de memoria
  // Para esta scope
}

```