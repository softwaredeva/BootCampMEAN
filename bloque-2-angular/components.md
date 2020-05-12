# Components

Un componente controla una parte de nuestra pantalla llamada vista, y estos se utilizan definiendo el nombre del componente y se declara como un tag de html, utilizarás los componentes para darle estructura a tu desarrollo así como para reutilizar partes del código a lo largo de la aplicación.

Cada componente cuenta con una clase la cuál se genera una instancia al ser cargado el componente en la pantalla

Además de la clase cada componente tiene una plantilla html la cuál puede y tendrá normalmente otras plantillas de vistas anidadas

## Sintaxis de plantilla

En la plantilla se podrá utilizar cualquier elemento de html que ya conocemos así como los elementos que angular agrega como las directivas *ngFor, *ngIf, ngClass, etc. y los elementos del "data binding".

Además de esto podremos agregar etiquetas personalizadas y será aqui donde se cargue nuestro componente creado por ejemplo:

```html
<h2>Products List</h2>

<p><i>Select a product from the list</i></p>
<ul>
  <li *ngFor="let product of products" (click)="selectProduct(product)">
    {{product.name}}
  </li>
</ul>

<app-product-detail *ngIf="selectedProduct" [product]="selectedProduct"></app-product-detail>
```

Aquí nosotros incluimos el nuevo componente "product detail" el cuál mostrará más información sobre el producto.

[Referencia](https://angular.io/tutorial/toh-pt3)

## Actividad

1.- Crearemos nuestro primer componente que será una lista de productos, el cual contendrá la lista que recién creamos, para hacer esto utilizaremos el comando en la terminal de nuestra computadora, dentro de la carpeta del proyecto creado

```sh
$ ng generate component components/ProductsList
>
```

2.- Tenemos que cambiar el estilo del app.component al nuevo componente.

[Respuesta](./respuestas/components.md)

[<--](./README.md)
