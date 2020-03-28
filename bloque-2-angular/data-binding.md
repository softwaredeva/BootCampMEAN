# Data binding

En angular utilizamos {{ variable }} (Interpolation) dentro de la sintaxis del html para que angular "renderee" el valor de una variable.

```html
<!-- component.html -->

   <h1>{{title}}</h1>
   <h2>My favorite food is: {{myFood}}</h2>

```

```ts
// component.ts

  title: string = 'Tour of Heroes';
  myFood: string = 'Sushi';
```

Podemos hacer llamadas a funciones de la siguiente forma:

```html
<p>The sum of 1 + 1 is not {{1 + 1 + getVal()}}.</p>
```

Lo que NO podemos utilizar dentro de {{}} es:

* Asignaciones (=, +=, -=, ...)
* Operadores como "new", "typeof", "instanceof", etc.
* Múltiples expresiones con "**;**" ó "**,**"
* Los operadores incrementales y decrementales **++** y **--**
* Algunos operadores de  ES2015+

Cuando buscamos ligar una variable al valor de una propiedad de un tag html:

```html
<img [src]="itemImageUrl2">
```

Podemos acceder directamente desde el html a la instancia "typescript" de los elementos HTML usando las variables de referencia:

```html
<label>Type something:
  <input #customerInput>{{customerInput.value}}
</label>
```

También podemos ejecutar sentencias que respondan a eventos

```html
<button (click)="deleteHero()">Delete hero</button>
```

Lo que NO podemos utilizar dentro de nuestras sentencias es:

* new
* Los operadores incrementales y decrementales, ++ y --
* Los operadores de asignación, += y -=
* Los operadores "bitwise", | y &
* El operador "pipe"

Doble vía:

```html
<input [(ngModel)]="userName" placeholder="Nombre"/>
```

Atributos:

```html
<button [attr.aria-label]="help">help</button>
```

Clases:

```html
<div [class.active]="isActive">Active</div>
```

Estilo:

```html
<button [style.color]="isActive ? 'red' : 'green'">
```

[Referencia (template-syntax)](https://angular.io/guide/template-syntax)  
[Referencia](https://angular.io/tutorial/toh-pt1)

## Actividad

En nuestro archivo "app.component" agregar los elementos necesarios para que se pueda mostrar el valor de un objeto de tipo "Producto" con las propiedades: id, name, cost e image, declarado en el controlador de la vista, usando el siguiente estilo y html.

```html
<!-- app.component.html -->


<div class="buttonInner">
  <div class="imageContainer">
    <img src="link/a/la/imagen" alt="texto alternativo">
  </div>
  <h1>Nombre del producto</h1>
  <div class="priceContainer">
    <h2>345</h2>
    <mat-icon color="accent">arrow_right_alt</mat-icon>
  </div>
</div>
```

```scss
// app.component.scss

.buttonInner{
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  padding: 1em;

  .imageContainer{
    height: 4em;
    width: auto;
    img{
      height: 100%;
      width: auto;
    }
  }
  h1{
    width: 100%;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .priceContainer{
    display: flex;
    align-items: center;
  }
}
```

[Respuesta](./respuestas/data-binding.md)

[<-- Atrás](./README.md)
