# 2 Ejecutar js que modifique una página en consola

## Pasos

* Abrir cualquier explorador web en cualquier página
* Abrir menú de desarrollador
* Abrir inspector web
* Seleccionar "Consola"
* En la linea de entrada de comandos ">" ingresar código js

```js
// https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Object/prototype

var DOMmods = function(tagName) {
  this.element = document.getElementsByTagName(tagName)[0];
};

DOMmods.prototype.updateElement = function(innerHTML) {
  if(this.element)
  this.element.innerHTML = innerHTML;
};

let myDOMmods = new DOMmods('h5');

myDOMmods.updateElement('Epidemia');
```

[<--](../../web-broswer-js-basico.md)
