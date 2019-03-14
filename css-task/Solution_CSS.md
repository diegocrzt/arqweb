# Listado de Tareas - Cambio de estilo

Modificar el estilo del `HTML` proveído en el archivo [index.html](index.html) y disponibilizar los cambios en [github pages](https://pages.github.com/).

## Pre-requisitos

* Leer el soporte [dado en clases](../CSS.md) y/o las referencias proporcionadas y aplicar las reglas `CSS` necesarias para modificar el estilo del archivo `HTML` proveído, acorde a los cambios solicitados en la sección siguiente.

## Cambios de estilo

### En el cuerpo de la página

* Cambiar el color del fondo de la página.
* Cambiar el formato del texto usando [Overpass](https://fonts.google.com/specimen/Overpass?selection.family=Overpass), o algún otro tipo de tipografía de google.
* _(Bonus!)_ Reducir el tamaño del `div` container y centrarlo con respecto al `body`.

### Cambiar el formato de títulos

* Cambiar el tamaño de los títulos `<h1>` y `<h2>` por los tamaños `1.7em` y `1.2em` respectivamente.
* Cambiar el color de los títulos.

### Listado

* Remover la viñeta de la lista de tareas.
* Remover el margen de la lista de tareas.
* _(Bonus!)_ Colocar una linea sobre el texto dentro del label de todas las tareas completadas.

### Botones

* Cambiar el color, fondo y borde de los botones.
* Cambiar a redondeado el borde de los botones.
* Cambiar el cursor a `pointer` y el formato del botón cuándo el mouse es dispuesto encima.
* _(Bonus!)_ Diferenciar los colores para los botones agregar, editar y borrar.

### Cuadro de texto

* Cambiar el margen y tamaño del cuadro de texto, en ancho y alto.
* Redondear el borde cuadro de texto.
* _(Bonus!)_ Cambiar el color del borde de texto y la sombra cuando el cursor se encuentra dentro de el.

### Criterios

* Escribir las reglas CSS que apliquen los cambios sugeridos. 
* Poner en práctica las buenas prácticas, puedes consultar éste [link](https://code.tutsplus.com/tutorials/30-css-best-practices-for-beginners--net-6741).
* No comprimas el archivo CSS.
* El repositorio debe contener el archivo HTML con los estilos aplicados (los estilos de ser posible en un fichero externo).
* Los estilos CSS aplicados `DEBEN` ser válidos. Asegurate de usar un validador como [éste](https://jigsaw.w3.org/css-validator).
* La información del estudiante junto con los enlaces al repositorio y la página `DEBEN` ser enviados antes del `miércoles 13 de marzo de 2019` a las `23:59:59` por medio del siguiente [formulario](https://goo.gl/forms/UbLn3CjbQwOy3qbR2).
* Usar tu creatividad e imaginación! 😉

## Consideraciones Adicionales

* No se puede utilizar ningún tipo de generador de estilos.
* No utilizar ningún framework CSS.
* No es necesario hacer el `reset CSS`.
* Si estas inspirado, no dudes en aplicar más reglas CSS para mejorar el estilo de la página.
* Es importante completar éste TP porque los enunciados siguiente se basaran sobre ésta misma aplicación.

## Solución

[Aquí](./) pueden encontrar una propuesta de solución al problema con el fuente.

Algunos puntos importantes que se tendran en cuenta para la evaluación son:

* El CSS debe ser válido (cómo solicitaba el enunciado).
* Las reglas `inline` se debían evitar. El HTML propuesto ya contenía las clases que se necesitaban,por lo que no era necesario modificar en nada el HTML, salvo para agregar el [link](./index.html) al archivo de [estilos](./primary.css).
* Los puntos bonus y los comentarios hacen la diferencia entre una buena nota y una muy buena nota! 😉

## Conclusión

Lo interesante de éste ejercicio era entender que el archivo de estilos permite modificar el diseño visual del HTML de manera independiente. Los ficheros de estilo no afectan la estructura del árbol de etiquetas, pero hacen uso de él mediante los selectores para aplicar las reglas de diseño.

**Si no pudiste realizar el trabajo, lee la solución y trata de comprenderla dado que los futuros TPs requeriran entender el selector y las reglas CSS.**
