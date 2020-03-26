# Conceptos angular

## Módulos

Los NgModules en angular declara un contexto de compilación para un conjunto de componentes que están relacionados dado sus capacidades o su flujo de trabajo.

Todas las aplicaciones de angular tendrán un módulo "root" llamado "AppModule", el cuál inicialzará nuestra aplicación.

Las funcionalidades y componentes de los módulos podrán importarse en otros módulos.

Los módulos nos darán la capacidad de organizar nuestro código para poder re-usarlo en diferentes partes del proyecto o en diferentes proyectos.

## Componentes

Cada aplicación angular contiene por lo menos un componente, el componente raíz que conecta uun jerarquía de componentes con el "DOM". Cada componente está asociado con un "template" de HTML que define la vista que se mostrá al usuario así como la lógica de la información necesario para esta vista.

## Servicios y "dependency injection"

Cuando tenemos datos que no están asociados a una vista en especifico y queremos compartirlos a lo largo de los diferentes componentes de la aplicación, utilizamos los servicios. Estos serán de tipo "injectable" y podrán ser utilizados como dependencias dentro de nuestros componentes.

La inyección de dependencias "dependency injection" nos ayudará a mantener un código legible y mantenible, esto al quitar responsabilidades de manejo de datos a los componentes y dejárselo a los servicios. Estos serán cargados bajo el patrón de diseño "singleton" manteniendo eficiente nuestra aplicación.

## Routing

Angular provee un módulo llamado "Router" el cuál nos ayudará a ligar el path de navegación con los diferentes estados de nuestra aplicación.

Esto para proveer las funcionalidades de:

* Entrar utilizando un url específico
* Utilizar links para que nuestro explorador abra nuevas páginas.
* Funciones de "back" y "forward" de nuestro explorador.

## Diagrama

<img src="../imgs/angular-overview.png"
alt="JS classes" width="640" height="auto" style="border: solid gray 1px"/>

[Referencia ->](https://angular.io/guide/architecture)