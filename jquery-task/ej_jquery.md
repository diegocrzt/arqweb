# Listado de Tareas - Usando jQuery

El objetivo de éste trabajo práctico es familiarizarse un poco con la librería `jQuery` en lugar de la librería 
`ajax.js` proveída en el TP anterior. 
Para ello, seguiremos usando el API `https://task-backend-fpuna.herokuapp.com/tasks/` publicado en internet.

Puedes partir del mismo fuente de tu solución del `TP CSS` y aplicar los pasos descriptos en la sección de Pre-requisitos.
O también puedes usar el código del `TP JS` y adaptarlo para reemplazar solo las partes requeridas.

Lo que debes hacer es completar el archivo `todolist.js` añadiendo lógica necesaria para permitir el funcionamiento de 
la página usando métodos que provee la librería `jQuery`. Para ello `DEBES` leer la 
[documentación oficial](https://api.jquery.com/) del sitio de `jQuery`. 

> En ésta ocasión no utilizaremos el archivo `ajax.js` por lo que puedes eliminarlo de tu repositorio al igual que la
etiqueta `<script type="text/javascript" src="js/ajax.js" async></script>` en el index.

## Pre-requisitos
* Leer el soporte dado en clases y/o las referencias.
* Retomar el código de tu solución del trabajo de CSS y agregar el archivo `todolist.js` en la carpeta `js`
 y colocar las siguientes etiquetas al final del cuerpo de la página (el orden es importante):
```html
<script src="http://code.jquery.com/jquery-3.3.1.min.js" integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8="
        crossorigin="anonymous">
</script>
<script type="text/javascript" src="js/todolist.js" async></script>
```
* Reemplazar la primera línea de código del archivo `todolist.js` por ésta
```js
(($) => {
```
* Reemplazar la última línea de código del archivo `todolist.js` por ésta
```js
})(jQuery);
```

## Cómo funciona el API?
Para rememorar ésto, lee [aquí](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/problem/Ej_JS.md#funcionamiento-de-la-api).

## Cómo hacer una llamada AJAX al API usando jQuery?
Para hacer la llamada ajax debes leer la documentación oficial que se encuentra en la sección de referencias.
`jQuery` provee varias opciones posibles.

_* Tener en cuenta que `DEBES` leer bien las especificaciones de la función que utilizaras. Dependiendo del método o 
las funciones que utilices puede que sea o no necesario usar el método `JSON.parse` dado que jQuery podría encargarse de 
hacer tal conversión._

## Usando `jQuery`
* ITEM 0: Busca una función equivalente a `document.onreadystatechange` proveída por `jQuery` y asegurate que dentro
se ejecute una función que llame al API con el método `GET` para recuperar la lista de tareas existentes. [más detalles](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/problem/js/todolist.js#L32-L36) 
* ITEM 1: Dentro de la función `addTask` llamar al API con el método `POST` para crear una nueva tarea. 
[más detalles](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/problem/js/todolist.js#L82-L88) 
* ITEM 2: Dentro de la función `editTask` llamar a la API con el método `PUT` cuando la descripción de la tarea es  
modificada. [más detalles](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/problem/js/todolist.js#L186-L193) 
* ITEM 3: Dentro de la función `addOnChangeEvent`, en el evento `onchange` del checkbox, recuperar el nuevo valor del 
estado de la tarea, (si el checkbox está marcado significa que la tarea está terminada, sino, sigue pendiente) y 
colocar la tarea entre la lista de tareas que corresponda (tareas completadas o tareas pendientes). Una vez hecho ésto, 
llamar al API con el método `PUT` para guardar el nuevo estado de la tarea. [más detalles](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/problem/js/todolist.js#L109-L115) 
* ITEM 4: Dentro de la función `removeTaskFromList`, eliminar la tarea en cuestión del DOM HTML.
[más detalles](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/problem/js/todolist.js#L240)
* ITEM 5: Dentro de la función `removeTask`, llamar al API con el método `DELETE` para borrar la tarea del servidor. 
[más detalles](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/problem/js/todolist.js#L249-L254)
* _Bonus!_ ITEM 6: Agrega un elemento en la página HTML para mostrar los mensajes de error, y desde la función
`showError()` haz visible o invisible el elemento para mostrar el texto de error. El error debe 
mostrarse solo por 5 segundos, luego de ésto, debe desaparecer. No dudes en las clases css `error-bar`, `hide-bar` y
`show-bar` en el archivo de estilos. [más detalles](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/problem/js/todolist.js#L46-L48)
* _Bonus!_ Reemplazar `TODAS` las funciones de manipulación de `DOM` y eventos usando jQuery. Es una 
buena practica que si usamos una librería unifiquemos el uso de sus funciones.

### Criterios
* Completa las funciones solicitadas para que la página sea funcional usando los [métodos HTTP](../../http_protocol/README.md)
 vistos en las clases anteriores y la API proveída.
* No comprimas el archivo JS.
* Preferiblemente, no deben aparecer errores a causa del código en la consola del navegador al cargar la página.
* El repositorio debe contener el archivo HTML, CSS y los archivos JS modificados con las funciones solicitadas, y la 
applicación debe estar deployada usando github pages.
* La información del estudiante junto con los enlaces al repositorio y la página `DEBEN` ser enviados antes del 
`TBA` a las `23:59:59` por medio del siguiente [formulario](https://goo.gl/forms/e4ajnmhqAu61uadA2).

## Consideraciones Adicionales
* Dado que el API es compartido entre todos los estudiantes, deben tener en cuenta que tareas pueden ser añadidas, 
borradas o editadas por otros usuarios.
* Es importante completar éste TP porque los enunciados siguiente se basaran sobre ésta misma aplicación.
* No te olvides que si el tipo de dato está especificado como `json`, jQuery podría convertir la cadena en un objeto
por lo que no necesitas parsear la respuesta (puedes remover JSON.parse()).

## Referencias
* [Contenido visto en clase](https://github.com/diegocrzt/diegocrzt.github.io/blob/master/js-task/lesson/JS.md)
* [Documentación de la API jQuery](https://api.jquery.com/)