# Notas de estilo para HTML(5)

## HTML Conveciones de Codificación

Los Desarrolladores Web a menudo no están seguros sobre el estilo de codificación y la sintaxis para usar HTML.

Entre el 2000 y el 2010, muchos desarrolladores web convertían HTML en XHTML.

Con XHTML, los desarrolladores fueron forzados a escribir, validar y tener un “código bien formado” ó “Buenas prácticas en el código”.

HTML5 es un poco menos riguroso cuando se trata de la validación de código.

Con HTML5 tú debes crear tu propia buena práctica, guía de estilo y convenciones de código.

## Se inteligente y la prueba del futuro

Un consecuente uso de estilo puede hacer más fácil para otros entender y usar tu HTML.

En el futuro, programas como lectores de XML, podrían leer tu HTML.

Usar la sintaxis de una estructura bien formada similar a XHTML puede ser una buena práctica.

Siempre mantén tus buenas prácticas de estilo de manera ordenada y limpia.


## Use Correcto del Tipo de Documento

Siempre declara el tipo de documento en la primera línea de tu documento:

```
<!DOCTYPE html>
```

Si deseas consistencia en tus etiquetas puedes declarar el tipo de documento también de la siguiente manera:

```
<!doctype html>
```
## Uso de minúsculas en los nombres de los elementos

HTML5 permite mezclar minúsculas y mayúsculas en los nombres de los elementos.

Nosotros recomendamos usar minúscula en los nombres de los elementos.

Mezclar nombres con Mayúsculas y minúsculas es malo, los desarrolladores esta acostumbrados a usar nombre en minúsculas (como en xhtml) las minúsculas se ve más limpio y son fáciles de escribir mal:

```
<SECTION>
  <p>This is a paragraph.</p>
</SECTION>
```
#### Mala práctica:
```
<Section>
  <p>This is a paragraph.</p>
</SECTION>
```
#### Buena práctica:
```
<section>
  <p>This is a paragraph.</p>
</section>
```
Es recomendable que todos los elementos en HTML5 sean cerrados (por ejemplo el elemento <p>).


#### Mala práctica:

```
<section>
  <p>This is a paragraph.
  <p>This is a paragraph.
</section>
```
#### Buena práctica:

```
<section>
  <p>This is a paragraph.</p>
  <p>This is a paragraph.</p>
</section>
```
## Elementos vacíos de HTML sin cierre:
En HTML5, es opcional cerrar elementos vacios.

Esto esta permitido:

```
<meta charset="utf-8">
```
Esto tambien esta permitido:

<meta charset="utf-8" />
El Slash (/) es requerido en XHTML y XML.

Si espera software en XML para acceder a la página, puede ser una buen idea mantenerlo.

## Uso de minúscula en los nombre de atributos:
HTML5 permite mezclar en minúscula y mayúscula los nombres de atributos.
Nosotros recomendamos usar minúscula en los nombres de los atributos:
Mezclar nombres con Mayúsculas y minúsculas es malo, los desarrolladores esta acostumbrados a usar nombre en minúsculas (como en xhtml) las minúsculas se ve más limpio y son fáciles de escribir mal:

#### Mala práctica:

```
<div CLASS="menu">
```
#### Buena práctica:

```
<div class="menu">
```
## Comillas
HTML5 permite usar atributos sin las comillas.

Nosotros recomendamos usar las comillas en los valores de los atributos:

Tienes que usar las comillas si el valor contiene espacios, mezclar estilos no es bueno, los valores de las comillas son fáciles de escribir. Esto podría no funcionar, porque el valor contiene espacios:


```
<table class=table striped>
```

### Esto funcionará:

```
<table class="table striped">
```
## Atributos en las imagenes:
Siempre usa el atributo “alt” con imágenes. Es importante cuando la imagen no se visualiza, ya que este “alt” indicará que imagen está siendo colocada ahí.

```
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px">
```

Siempre define el tamaño de la imagen. Esto permite que el navegador guarde el espacio de la imagen antes de la carga evitando un parpadeo innecesario.

```
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px">
```

## Espacios y signos de igualdad:
Los espacios alrededor del signo “igual” no son buena práctica:

```
<link rel = "stylesheet" href = "styles.css">
```

Menos espacio es más fácil de leer:
```
<link rel="stylesheet" href="styles.css">
```

## Evitar largas líneas de código
Cuando usamos un editor de texto, el inconveniente de hacer scroll hacia la derecha e izquierda para leer el HMTL5.

Trata de evitar que tus líneas de código no sea más largo de 80 caracteres.

## Líneas en blanco e indentación:
No agregues líneas en blanco sin ninguna razón.

Para que sea más fácil de leer, agrega líneas blancas para separar largos y gruesos bloques de código.

Para que sea más fácil de leer, añade 2 espacios de indentación. No uses TAB.

No uses líneas blancas o indentación que no sea necesaria, no es necesario usar líneas blancas entre cortos y relacionados artículos o data, no es necesario indentar cada elemento:

#### Innecesario:
```
<body>

  <h1>Famous Cities</h1>

  <h2>Tokyo</h2>

  <p>
    Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
    and the most populous metropolitan area in the world.
    It is the seat of the Japanese government and the Imperial Palace,
    and the home of the Japanese Imperial Family.
  </p>

</body>
```

#### Buena práctica:
```
<body>

<h1>Famous Cities</h1>

<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.
It is the seat of the Japanese government and the Imperial Palace,
and the home of the Japanese Imperial Family.</p>

</body>
```

#### Ejemplo de Tabla:
```
<table>
  <tr>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>A</td>
    <td>Description of A</td>
  </tr>
  <tr>
    <td>B</td>
    <td>Description of B</td>
  </tr>
</table>
```

#### Ejemplo de Lista:
```
<ol>
  <li>London</li>
  <li>Paris</li>
  <li>Tokyo</li>
</ol>
```

## Omitir <html> y <body>?
En HTML5 estándar, la etiqueta <html> y la etiqueta <body>  pueden ser omitidas.

El siguiente código puede ser validado en HTML5:

#### Ejemplo
```
<!DOCTYPE html>
<head>
  <title>Page Title</title>
</head>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>
```


Nosotros no recomendamos omitir estas etiquetas.

El documento es el elemento raíz, es el lugar recomendado para especificar a la página el lenguaje:
```
<!DOCTYPE html>
<html lang="en-US">
```
Declarar el lenguaje es importante para la accesibilidad de aplicaciones, como puede ser las herramientas de SEO.

Omitirlos puede dañar el DOM y el XML software.

Omitir puede producir error en el navegadores antiguos como IE9.

## Omitir <head>?
El estándar de HTML5 la etiqueta <head> puede ser omitida.

Por default, los navegadores añadirán los elementos antes, a un elemento predeterminado.

Puedes reducir la complejidad de HTML5, omitiendo la etiqueta <head>.

#### Ejemplo
```
<!DOCTYPE html>
<html>
<title>Page Title</title>

<body>
  <h1>This is a heading</h1>
  <p>This is a paragraph.</p>
</body>

</html>
```

Omitir etiquetas es poco familiar para los desarrolladores web. Necesita tiempo para establecerlo como una guía.

## Meta Data
La etiqueta <title> es un elemento requerido en HTML5. Mantén el título lo más claro posible.

```
<title>HTML5 Syntax and Coding Style</title>
```
Para asegurar la interpretación adecuada y la correcta indexación de motores de búsqueda, ambos lenguajes y la codificación de caracteres debería ser definida lo más pronto posible en el documento:

```
<!DOCTYPE html>
<html lang="en-US">
<head>
  <meta charset="UTF-8">
  <title>HTML5 Syntax and Coding Style</title>
</head>
```
## Comentarios en HTML
Los comentarios cortos deben escribirse en una sola línea, de manera espaciada <!-- and a space before -->:
```
<!-- This is a comment -->
```
Los comentarios largos abarcan muchas líneas, debería ser escrito <!-- and --> con líneas separadas:

```
<!--
  This is a long comment example. This is a long comment example. This is a long comment example.
  This is a long comment example. This is a long comment example. This is a long comment example.
-->
```
Los comentarios largos son fáciles de observar, si están indentando con dos espacios.

## Hojas de Estilo
Usa la sintaxis simple para linkear las hojas de estilo (El tipo de atributo no es necesario):

```
<link rel="stylesheet" href="styles.css">
```
Los estilos cortos pueden ser escritos de manera comprimida, en una línea, como el siguiente ejemplo:

```
p.into {font-family: Verdana; font-size: 16em;}
```
Los estilos largos deben ser escritos en múltiples líneas:

```
body {
  background-color: lightgrey;
  font-family: "Arial Black", Helvetica, sans-serif;
  font-size: 16em;
  color: black;
}
```

Coloca el bracket ({}) en la misma línea del selector, usa un espacio antes de abrir el bracket.

Usa dos espacios para la indentación. Usa los dos puntos (:) entre la propiedad y el valor.

Usa el espacio después de la coma (,) o punto y coma (;). Usa punto  coma (;) después de cada propieda:valor sin espacios.

Evita las líneas de 80 caracteres. Agrega un espacio después y coma (,) o punto y coma (;), es una regla general en todos los tipos de escritura.


## Cargando JavaScript en HTML5
Usa una sintaxis simple para cargar los scripts externos ( El tipo de atributo no es necesario):
```
<script src="myscript.js">
```
## Accediendo a los elementos de HTML con JavaScript
Una consecuencia de usar un estilo de HTML “desordenado”, podría resultar un JavaScript con errores.

Existen dos tipos de declaración que puede producir diferentes resultados:

#### Ejemplo

```
var obj = getElementById("Demo")

var obj = getElementById("demo")
```

Es posible usar las mismas convenciones de nombramiento (como javaScript) en HTML.

Visita la guía de Estilo de JavaScript.

## Utilizar minúsculas en los nombres de los Archivos
Muchos de los servidores web (Apache, Unix) diferencia entre mayúsculas y minúsculas con el caso de nombramiento en los archivos, en este caso deberíamos seguir las siguientes reglas:

london.jpg no puede ser London.jpg

Otro servidor web (Microsoft, IIS) no distinguen entre mayúsculas y minúsculas, entonces puede ser escrito de la siguiente manera:

london.jpg puede ser London.jpg o london.jpg

Si tu usas una mezcla de mayúscula y minúscula, tienes que ser extremadamente consistente.

Si se mueve de un caso en que no sea importante el reconocimiento de mayúsculas a minúsculas a casos en los que sí importa en un servidor web cualquier pequeño error puede romper tu página.

Para evitar estos problemas, siempre usa minúscula en el nombramiento de archivos (si es posible).

## Extensiones de Archivos
Los archivos HTML deben tener una extensión .html o .htm

Los archivos CSS deben tener una extensión .css

Los archivos de JavaScript deben tener una extensión .js

## Diferencias entre .html y .htm

No existe diferencia entre las extensiones de .htm y .html, ambas pueden ser tratadas como HTML por cualquier navegador web o servidor web.

Las diferencia son culturales.

.htm “huele” a un sistema temprano llamado DOS donde el límite de extensiones es de 3 caracteres, mientras que .html “huele” a UNIX un sistema que no tiene limitación en sus caracteres.


## Diferencias Técnicas
Cuando una URL no especifica el nombre de archivo ( como http://www.w3schools.com/css/), el servidor retorna por defecto el nombre del archivo.

Los nombre comunes por defecto son index.html, index.htm, default.html y default.htm

Si tu servidor es configurado solo con “index.html” como nombre por defecto, tu archivo debe ser nombrado como “index.html” no “index.htm”

Sin embargo, los servidores pueden ser configurados con más de un nombre por defecto y normalmente puedes configurar tantos nombres de archivos por defecto como necesites.

De todas formas, la extensión completa para HTML es .html y no existe ninguna razón por la cual no puede ser usada.
