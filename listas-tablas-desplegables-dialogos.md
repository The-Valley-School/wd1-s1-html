## LISTAS

La etiqueta ul nos permite crear un listado dentro de HTML, cada elemento de la lista estará identificado con la etiqueta li. En caso de quere hacer una lista ordenada podemos usar ol

- Lista

```
<p>Listado de la compra</p>
<ul>
	<li>Fruta</li>
	<li>Carne</li>
	<li>Pescado</li>
	<li>Yogures</l>
</ul>
```

- Lista ordenada

```html
<p>Top Forbes</p>
<ol>
	<li>Elon Musk</li>
	<li>Jeff Bezos</li>
	<li>Warren</li>
	<li>Bill</li>
</ol>
```

En las listas ordenadas podemos indicar con un atributo el número por el que queremos que empiece. De igual manera, podemos decir que haga una cuenta hacia atrás en vez de hacia delante

```html
<p>Top Forbes</p>
<ol start="5" reversed>
	<li>Elon Musk</li>
	<li>Jeff Bezos</li>
	<li>Warren</li>
	<li>Bill</li>
</ol>
```

Podemos también anidar listas:

```html
<p>Top Forbes</p>
<ol>
	<li>
		Elon Musk
		<ul>
			<li>Tesla</li>
			<li>SpaceX</li>
	</li>		
	<li>Jeff Bezos</li>
	<li>Warren</li>
	<li>Bill</li>
</ol>
```

## TABLAS

También podemos hacer tablas en HTML, para ello utilizaremos la etiqueta table, para cada fila la etiqueta tr y para cada columna la etiqueta td

Para que la tabla tenga aspecto visual de tabla podemos incluir dentro de la etiqueta table un atributo **border**

```html
<table border="1">
	<tr>
		<td>Manzanas</td>
		<td>3</td>
		<td>2€</td>
	</tr>
	<tr>
		<td>Peras</td>
		<td>6</td>
		<td>3,5€</td>
	</tr>
	<tr>
		<td>Meló</td>
		<td>1</td>
		<td>6€</td>
	</tr>
	<tr>
		<td>Naranjas</td>
		<td>6</td>
		<td>3€</td>
	</tr>
</table>
```

Para incluir la cabecera usaremos la etiqueta th.

Para tablas grandes tenemos la estructura:

- thead para la cabecera
- tbody para el cuerpo de la tabla
- tfoot para el pie de la tabla

    

```html
<table border="1">
	<thead>
		<tr>
			<th>Frutas</th>
			<th>Unidades</th>
			<th>Precio</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Manzanas</td>
			<td>3</td>
			<td>2€</td>
		</tr>
		<tr>
			<td>Peras</td>
			<td>6</td>
			<td>3,5€</td>
		</tr>
		<tr>
			<td>Meló</td>
			<td>1</td>
			<td>6€</td>
		</tr>
		<tr>
			<td>Naranjas</td>
			<td>6</td>
			<td>3€</td>
		</tr>
	</tbody>
	<tfoot>
		<tr>
			<td></td>
			<td>16</td>
			<td>14,5€</td>
		</tr>
	</tfoot>
</table>
```

 
## DETAILS

El objetivo de la etiqueta details es poder crear un elemento desplegable que los usuarios 

puedan expandir y contraer para mostrar información. La estructura es la siguiente:

    

```html
<details>
	<summary>Título desplegable</summary>
	<p>Información desplegable</p>
</details>
```

   

La información desplegable puede ser cualquier contenido, no hace falta que sea un párrafo.

## DIÁLOGOS EMERGENTES

Podemos utilizarlos para mostrar avisos o alertas al usuario. Normalmente, a la hora de enviar este tipo de alertas utilizamos en javascript la función alert. Ahora podemos hacerlo directamente desde HTML5. Pondremos el atributo open para que salga directamente la modal.

   

```html
<dialog open>
	<p>¡Bienvenidos al máster!</p>
</dialog>
```

A través de JS podríamos jugar con estas modales, abriéndolas y cerrándolas a nuestro gusto.
