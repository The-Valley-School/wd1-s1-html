
HTML es el lenguaje que nos va a permitir estructurar y organizar el contenido de una página web. Con su estructura en árbol que hace que tenga diferentes nodos y cada uno de ellos pueda contener hijos.

En HTML trabajamos con etiquetas. Las etiquetas tienen la siguiente estructura:

 

```jsx
<apertura-etiqueta>CONTENIDO</cierre-etiqueta>
```

  

Aunque hay algunas, como por ejemplo la etiqueta de img que es única.

 

```jsx
<etiqueta>
```

Estas etiquetas también pueden tener atributos, por ejemplo un atributo de color que indica el color de la letra del párrafo:

```jsx
<p stylet="color:blue;">Párrafo de ejemplo</p>
```

 

**ESTRUCTURA DE UN DOCUMENTO HTML**

Una vez dada esta visión global de HTML que vimos en el prework, vamos a empezar dando un un repaso a la estructura de un documento HTML.

La estructura típica de un documento HTML podría ser la siguiente:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

*Recordad que esta estructura podéis montarla en VSC escribiendo el signo ! y pulsando enter.*

**ETIQUETA DOCTYPE**

Lo primero que tenemos es la etiqueta <doctype> que indicará al navegador la versión de HTML que se está utilizando en el documento:

```html
<!DOCTYPE html>
```

Esta etiqueta hace referencia al estándar actual, e indica al navegador que estamos usando HTML 5.

**ETIQUETA HTML**

La etiqueta <html> es la raíz del documento. Como hemos comentado, HTML tiene forma de árbol, por lo tanto, la etiqueta <html> será el nodo del que cuelguen todas las demás etiquetas.

**ETIQUETA HEAD y BODY**

La etiquetas head y body son los únicos nodo hijo que puede tener una etiqueta html. A partir de ahí, la etiqueta head contiene todo el contenido que no se muestra en el navegador, mientras que en la etiqueta body meteremos todo aquel contenido que sí queremos mostrar.

 

```html
<html>
<head>
    CONTENIDO QUE NO SE MUESTRA
</head>
<body>
    CONTENIDO QUE QUEREMOS MOSTAR
</body>
</html>
```

 

Vamos a profundizar  en el contenido que puede tener la etiqueta HEAD. Hemos comentado que nos permite introducir información que no muestra por pantalla, ¿qué contiene entonces? 

Contiene información muy diversa, desde el título de la página, codificación de ficheros, etiquetas para posicionamiento, enlaces a CSS, javascripts….

- **title** Contiene el título del documento, el cual se mostrará en los navegadores en la parte superior, por ejemplo:

```html
<head>
     <title>Título de mi página web</title>
</head>
```

 

- **meta** Etiqueta que nos permitirá indicar información diversa. Por ejemplo la codificación del texto.

  

```html
<head>
     <meta charset="UTF-8">
</head>
```

  

Es posible añadir también etiquetas que ayuden al posicionamiento de la página:

  

```html
<head>
  <meta name="keywords" content="HTML, CSS, JavaScript" />
	<meta name="description" content="Contenido del curso de The Valley" />
</head>
```

- **link** También puede incluir etiquetas link que identifica una relación entre un documento actual y un recurso externo. Estos links los hemos utilizado mucho en el prework a la hora de incluir hojas de estilo css.

  

```html
<head>
     <link href="estilo.css" rel="stylesheet">
</head>
```

  

- **scripts** Al igual que las etiquetas link que utilizamos para incluir diferentes recursos externos, también podemos usar scripts dentro del head.

  

```html
<head>
     <script src="main.js"></script>
</head>
```

 

Recordad, que si lo incluimos dentro del head, se cargará en paralelo con el documento html y puede llevar a errores si estamos trabajando con DOM. Habría que incluir el atributo defer para que cargue al final.

- **base** Esta etiqueta nos ayuda a especificar la base para los destinos de los enlaces de una página. Por ejemplo:

  

```html
<head>
     <base href="http://www.mipagina.com/"></script>
</head>
```

 

Si yo incluyo un enlace en mi página con el atributo *href=”cursos”*, al pulsarlo la página a la que nos llevará será *http://www.mipagina.com/cursos.* Lo entenderéis mejor cuando trabajemos en los próximos vídeos con rutas.

**ETIQUETAS SEMÁNTICAS HTML5**

Dentro de la etiqueta body incluiremos todo el contenido que queremos mostrar, títulos, textos, imágenes…

Con la aparición de HMTL5, surgieron las etiquetas semánticas que nos ayudan a establecer estructuras en nuestra página, ayudando al navegador a entender mejor lo que mostrábamos.

![Untitled](%F0%9F%9F%A2%20SESIO%CC%81N%201%20-%20HTML%200ef5237969174592b386c7366a8b7900/Untitled.png)

**HEADER**

Hace referencia al título de nuestra página web y contenido importante que hiciese referencia a nuestra página. Normalmente título y logo, como ocurría en el ejercicio de final de prework.

```html
<header>
	<!-- Título de nuestra página y contenido importante sobre ella-->
</header>
```

**NAV**

Sección de nuestro documento HTML donde encapsularíamos la navegación, lo que viene siendo el menu de la página.

 

```html
<nav>
	<!-- Navegación de la página-->
</nav>
```

 

**MAIN**

Contenido principal de nuestra web.

 

```html
<main>
	<!-- Contenido principal de la web-->
</main>
```

**SECTION**

Etiqueta que utilizaremos para estructurar cada una de las secciones de nuestra página web. Si tomamos como referencia un periódico, estas serían la sección noticias, sección deportes…

```html
<section>
	<!-- Bloque de contenidos-->
</section>
```

**ARTICLE**

Los article podemos identificarlos, siguiendo el símil, como cada una de los artículos de esas secciones del periódico. Hace referencia a una parte de código que puede ser independiente.

Estos artículos nos los podríamos llevar a cualquier lado de la página web y seguirían teniendo significado propio.

```html
<article>
	<!-- Contenido con significado propio -->
</article>
```

**ASIDE**

Para indicar contenido no prioritario, como podría ser la sección de anuncios.

```html
<aside>
	<!-- Contenido no prioritario -->
</aside>
```

**FOOTER**

Sería el pie de página de nuestra web.

 

```html
<footer>
	<!-- Pie de página -->
</footer>
```

  

Ejemplo:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estructura HTML</title>
</head>
<body>
    <header>
        <h1>Mi diario</h1>
    </header>
    <nav>
        <ul>
            <li><a href="">Menu 1</a></li>
            <li><a href="">Menu 2</a></li>
            <li><a href="">Menu 3</a></li>
            <li><a href="">Menu 4</a></li>
        </ul>
    </nav>
    <main>
        <section>
            <p>Top lecturas del mes</p>
            <article>
                <h2>Artículo 1</h2>
                <p> bla bla bla bla</p>
            </article>
            <article>
                <h2>Artículo 2</h2>
                <p> bla bla bla bla</p>
            </article>
            <article>
                <h2>Artículo 3</h2>
                <p> bla bla bla bla</p>
            </article>
        </section>
        <section>
            <p>Fulanito bla bla bla</p>
            <p>Menganito bla bla bla</p>
            <p>Pepito bla bla bla</p>
        </section>
    </main>
    <aside>
        <p>Aquí van los anuncios</p>
    </aside>
    <footer>
        <p>Copyright del periódico</p>
        <p>Acceder a redes sociales</p>
    </footer>
</body>
</html>
```

**DIV**

Para cualquier otro bloque, sin contenido semántico, utilizaremos DIV. En versiones anteriores de HTML donde no existían las etiquetas semánticas, todas las divisiones en bloques se hacían a nivel de DIV.

El principal uso que hacemos del DIV es a nivel visual, ya que nos ayuda a dividir en bloques cierta información, pudiendo luego asignarles un estilo propio.

Por ejemplo, si quisiésemos mostrar las valoraciones de un restaurante podríamos pintarlo de la siguiente manera:

 

```html
<body>
	<main>
		<section>
			<div class="review">
					<p> La comida riquísima </p>
					<p> 5 </p>
			</div>
			<div class="review">
					<p> Volveremos sin duda </p>
					<p> 5 </p>
			</div>
			<div class="review">
					<p> Tardaron mucho en servirnos. Precios altos </p>
					<p> 2 </p>
			</div>
		<section>
	</main>
</body>
```
