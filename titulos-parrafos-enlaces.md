Tras ver la estructura de un documento HTML y ver las etiquetas semánticas, vamos ahora a seguir viendo etiquetas.

### HEADING

Empezamos con la etiqueta HEADING, que nos va a valer para poner títulos en nuestras. Podemos utilizar de la etiqueta a h1 a la etiqueta h6 para estructurar nuestros títulos y subtítulos dentro de la página. Vamos del h1 al h6 por orden de importancia en nuestra página.

 

```html
<h1>Título 1</h1>
<h2>Título 2<h2>
<h3>Título 3</h3>
<h4>Título 4</h4>
<h5>Título 5</h5>
<h6>Título 6</h6>
```

 

### PÁRRAFO

Etiqueta que nos va a permitir escribir contenido dentro de nuestra página web. 

 

```html
<p>Párrafo de nuestra web</p>
```

 

Todos los párrafos comienzan ocupando una línea nueva, así que, si queremos un salto de línea debemos incluir un párrafo adicional

### SEMÁNTICA DEL TEXTO

Existen una serie de etiquetas que nos van a permitir poder darle una semántica al texto seleccionado, así como un estilo. Damos un repaso a las más utilizadas, pero es importante saber que existen otras que en determinado momento podemos llegar a utilizar. Os dejamos un enlace a la documentación que puede ayudar a ampliar esta info:

 

```
https://developer.mozilla.org/es/docs/Web/HTML/Element#sem%C3%A1ntica_del_texto_en_l%C3%ADnea
```

 

- **b** Procede la palabra bold y nos permite poner el texto en negrita

 

```html
<p><b>Este texto está en negrita<b></p>
```

- **br** Produce un salto de línea en el texto. Cuando queremos que el salto de línea tenga contenido semántico es mejor utilizar otro párrafo. En caso por ejemplo de un poema, donde hay saltos de línea pero no diferencia de contenido, es mejor utilizar br

 

```html
<p> 
	Naranjas, naranjas,<br>
	limones, limones,<br>
	tengo un amigo<br>
	que vale millones.
</p>
```

  

- **cite** Para marcar una referencia o el autor de un texto que citemos.

 

```html
<p><cite>Chaplin</cite> dijo: "Estoy a favor de la gente. No puedo evitarlo"</p>
```

  

- **em** Nos sirve para enfatizar el texto, puede estar anidado. Cuanto mayor anidamiento, mayor grado de énfasis.

 

```html
<p><em>Texto enfatizado</em></p>
```

  

- **i** Muestra el texto marcado en cursiva.

 

```html
<p><i>Texto en cursiva</i></p>
```

  

- **mark** nos permite marcar un bloque de manera resaltada como si estuviese marcado con un subrayador en amarillo

 

```html
<p><mark>Texto remarcado</mark></p>
```

  

- **q** para identificar una cita corta en línea.

 

```html
<p><q>Estoy a favor de la gente. No puedo evitarlo</q></p>
```

  

- **s** Texto tachado en horizontal

 

```html
<p><s>Texto tachado en horizontal</s></p>
```

  

- **strong** Para marcar con énfasis las partes importantes del texto.

 

```html
<p><strong>Parte importante del texto</strong></p>
```

  

- **u** Muestra el texto subrayado

 

```html
<p><u>Texto subrayado</u></p>
```

 

- **span**
    
    Hemos dejado para el final el elemento SPAN porque tiene bastante importancia y nos va a ser de gran ayuda a la hora de estructurar el documento.
    
    La etiqueta span sirve para aplicar estilos de texto agrupando elementos en línea. Podríamos decir que es un div pero en lugar de ser un contenedor en bloque es un contenedor en línea.
    
    Esta etiqueta nos sirve por ejemplo:
    
    - Mostrar varios elementos en línea.
    
    ```html
    <div>
    	<span class="social"> Facebook </span>
    	<span class="social"> Instagram </span>
    	<span class="social"> Pinterest </span>
    </div>
    
    <style>
    	.social{
    		background-color: blue;
    		color: white;
    		margin: 10px;
    		padding: 10px;
    	}
    </style>
    ```
    
    - Añadir unos estilos diferentes a una parte de un texto
    
     
    
    ```html
    <p>Hola me llamo <span style="color: red;">Edu</span></p>
    ```
    
     
    

### HIPERENLACES

Esta etiqueta nos va a permitir navegar a páginas dentro de la aplicación o a enlaces externos como otra web…

```html
<a href="https://www.thevalley.es">Ir a la página de The Valley</a>
```

Utilizamos la etiqueta a para ello. 

A su vez tienen una serie de propiedades que nos ayudan a trabajar con ellos.

- **href** es la atributo más importante, contiene una URL o fragmento de URL al cual apunta este enlace. Es obligatorio cada vez que usemos una etiqueta <a>:

 

```html
<a href="https://www.thevalley.es">Ir a la página de The Valley</a>
```

 

- **target** que nos indica donde desplegar la url enlazada:

  

```html

<!-- Carga URL en misma página (comportamiento por defecto) -->
<a target="_self" href="https://www.thevalley.es">Ir a la página de The Valley</a>

<!-- Carga URL en nueva página -->
<a target="_blank" href="https://www.thevalley.es">Ir a la página de The Valley</a>

<!-- Carga URL en la página padre -->
<a target="_parent" href="https://www.thevalley.es">Ir a la página de The Valley</a>

<!-- Carga URL en la página más alta -->
<a target="_top" href="https://www.thevalley.es">Ir a la página de The Valley</a>
```

- **rel** nos sirve para indicar la relación que tiene nuestra página, con la página a la que vamos.

  

```html

<!-- Para indicar que es un enlace de pago  -->
<a rel="sponsored" href="https://www.thevalley.es">Ir a la página de The Valley</a>

<!-- Para indicar a los navegadores que no siga el enlace -->
<a rel="nofollow"  href="https://www.thevalley.es">Ir a la página de The Valley</a>

```

 

- **download** nos sirve para poder descargar el contenido del enlace directamente.

 

```html
<a href="gatito.jpg" download="imagen.jpg">Ir a la página de The Valley</a>
```
