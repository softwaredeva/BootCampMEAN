# 1 Ejecutar js en consola

## Pasos

* Abrir cualquier explorador web en cualquier página
* Abrir menú de desarrollador
* Abrir inspector web
* Seleccionar "Consola"
* En la linea de entrada de comandos ">" ingresar código js

```js
// Iterativo
function fibonacci(num){
  var a = 1, b = 0, temp;

  while (num >= 0){
    temp = a;
    a = a + b;
    b = temp;
    num--;
  }

  return b;
}

// Recurción
function fibonacci(num) {
  if (num <= 1) return 1;

  return fibonacci(num - 1) + fibonacci(num - 2);
}

// Memorización (Memoization)
function fibonacci(num, memo) {
  memo = memo || {};

  if (memo[num]) return memo[num];
  if (num <= 1) return 1;

  return memo[num] = fibonacci(num - 1, memo) + fibonacci(num - 2, memo);
}

// https://medium.com/developers-writing/fibonacci-sequence-algorithm-in-javascript-b253dc7e320e
```

[<--](../../web-broswer-js-basico.md)
