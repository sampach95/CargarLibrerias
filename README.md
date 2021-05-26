# Cargar Librerias
Ahora que ya sabes que hay detrás de un mapa interactivo en leaflet, podemos comenzar a diseñar nuestras propias visualizaciones.

#### Antes de empezar te recomendamos instales algún editor de texto de tu preferencia, te recomendamos Notepad++ ya que es amigable para personas sin muchas nociones de programación e incluye todo lo necesario. Puedes descargarlo aquí. https://notepad-plus-plus.org/downloads/ 

### Iniciaremos creando una carpeta que aloje todos los archivos que iremos agregando a nuestro mapa, lo primero será crear un archivo de block de notas con extensión html, y lo abriremos con el editor de texto, en mi caso NotePad.

En las siguientes líneas iniciaremos con lo básico.

``` html
<html>
<head>
	<meta charset="utf-8">
	<title>Mapa E14C17_2</title>
  </head>
  <body>
  </body>
</html>
```
Asignaremos título a nuestro proyecto, en el ejemplo aparece como “Mapa E14C17” este título es el que aparecerá en la pestaña del navegador y en motores de búsqueda como Google.
En body, irá todo el código de nuestro mapa, pero antes es necesario cargar las librerías de Leaflet, para lo cual hay dos metodos:

### METODO 1: ARCHIVOS LOCALES

Para descargar Leaflet con este método es necesario ir a la página https://leafletjs.com/download.html


![screenshot](https://raw.githubusercontent.com/sampach95/CargarLibrerias/master/img/Imagen1.png )

Hay diferentes versiones, pero por el momento utilizaremos la versión estable, que es la primera de la lista. Dando click descargaremos un archivo .zip con todo lo necesario para desarrollar nuestro proyecto. 
Es necesario copiar el archivo .zip en la carpeta de nuestro proyecto y descomprimirlo.

![screenshot](https://raw.githubusercontent.com/sampach95/CargarLibrerias/master/img/Imagen2.png )

Las carpetas y archivos incluyen:
images: En está carpeta hay imágenes usadas en Leaflet, como íconos para el mapa.

- leaflet.css: Este archivo se encarga de darle estilo al mapa, de manera que todo se muestre correctamente, no es necesario editarlo, sin embargo es necesario incluirlo .

- leaflet.js: Este archivo nos permite utilizar los comandos de Leaflet.

- leaflet-src.js: Es similar a leaflet.js, salvo que contiene mas líneas de código, lo cual podemos notar si abrimos ambos, esto es porque leaflet-src.js está escrito por los desarrolladores de Leaflet. En caso de que requieras editar el código fuente modificaremos este archivo, si en cambio sólo te interesa utilizar las funciones de Leaflet utilizaremos leaflet.js, ya que es más compacto y funciona para desarrolladores principiantes.

Para continuar, debemos incluir dos archivos a nuestro codigo, el CSS y el JavaScript: 

``` html
<html>
<head>
	<meta charset="utf-8">
	<title>Mapa E14C17_2</title>
   <script src="lib/leaflet/leaflet.js"></script>
  <link rel="stylesheet" href="lib/leaflet/leaflet.css">
  </head>
  <body>
  </body>
</html>
```

### METODO 2: utilizar una CDN (Content Delivery Network). 

Con este método sólo es necesario navegar mas abajo en la página, https://leafletjs.com/download.html copiar y pegar lo que se muestra en el recuadro directamente en el código. 

![screenshot](https://raw.githubusercontent.com/sampach95/CargarLibrerias/master/img/Imagen5.png )

El código quedaría así:

``` html
<html>
<head>
	<meta charset="utf-8">
	<title>Mapa E14C17_2</title>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.6.0/dist/leaflet.css"
  integrity="sha512-xwE/Az9zrjBIphAcBb3F6JVqxf46+CDLwfLMHloNu6KEQCAWi6HcDUbeOfBIptF7tcCzusKFjFw2yuvEpDL9wQ=="
  crossorigin=""/>
	<script src="https://unpkg.com/leaflet@1.6.0/dist/leaflet.js"
  integrity="sha512-gZwIG9x3wUXg2hdXF6+rVkLF/0Vi9U8D2Ntg4Ga5I5BZpVkVxlJWbSQtXPSiUTtC0TjtGOmxa1AJPuV0CPthew=="
  crossorigin=""></script>
  </head>
  <body>
  </body>
</html>
```
#### Cada método tiene ventajas y desventajas, mientras el primer método puede ser tedioso, normalmente es mas estable en entornos  web, el segundo método es mas practico, pero requiere actualizaciones mas o menos frecuentes del código cuando es subido a un servidor, ya que al ser software libre esta sujeto a modificaciones a corto o largo plazo. 

### Para verificar que las librerías esten cargadas, en cualquier caso, seguiremos el siguiente procedimiento. 
Al abrir el archivo .html en el navegador, activaremos con F12 la consola, si se siguió el procedimiento correctamente, no habrá mensajes de error. Y podremos continuar.
Si desearas verificar para estar seguros, teclea “L” en la consola, si aparece como en la imagen, significa que la librería de Leaflet se cargó correctamente. 

![screenshot](https://raw.githubusercontent.com/sampach95/CargarLibrerias/master/img/Imagen3.png )

“L” es la clase que representa Leaflet, cualquier comando precedido por esta letra y un punto corresponde a un comando de Leaflet. Por ejemplo, lo que se muestra en la siguiente imagen:

![screenshot](https://raw.githubusercontent.com/sampach95/CargarLibrerias/master/img/Imagen4.png )



Siguiente Tutorial https://github.com/sampach95/CrearLienzoDelMapa

Haz click en el siguiente enlace para volver a la pagina inicial https://github.com/sampach95/ComoCrearMapasEnLaWebConLeaflet
