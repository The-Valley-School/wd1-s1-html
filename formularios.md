Como vimos en el prework, casi cualquier página web tiene formularios. Estos nos sirven para que el usuario pueda hacernos llegar una cierta información, ya sean:

- Sus datos para inscribirse a un curso
- Un email para suscribirse a una newsletter
- Nombre y apellidos para apuntarse a un correo….

**ESTRUCTURA DE FORMULARIO**

**FORM**

Para crear un formulario usaremos la etiqueta form:

 

```html
<form>
		<!-- Aquí va todo el contenido del formulario -->
</form>
```

 

Dentro de esta etiqueta podemos definir dos atributos:

- action que nos servirá para definir la localización donde se enviará la información que recoja el formulario
- method que indicará la forma que enviaremos la información.
    - **GET** → mandamos la información a través de variables en la URL
    - **POST** → enviamos la información a través de una transacción HTTP. Más segura.

 

```html
<form method="post" action="/">
		<!-- Aquí va todo el contenido del formulario -->
</form>
```

 

**FIELDSET**

Se trata de una agrupación de elementos comunes dentro del formulario y siembre va acompañada de la etiquete legend que le asigna un título descriptivo. Por ejemplo, en el caso de un registro a un gimnasio podríamos tener la agrupación de datos personales, la agrupación de datos bancarios y la agrupación de datos relacionados con el tipo de suscripción que se desea.

 

```html
<form method="post" action="/">
		<fieldset>
			<legend>Datos personales</legend>
		</fieldset>
</form>
```

**INPUT Y LABEL**

Para que el usuario pueda introducir información usamos las etiquetas input (igual que la de img, no hay apertura cierre). Con la etiqueta label damos información al usuario del contenido que tiene que meter dentro de ese input:

```html
<form>
	<label>
    Nombre
    <input>
	</label>
</form>

<!--  OTRA OPCIÓN -->

<form>
	<label for="nombre"> Nombre </label>
	<input id="nombre">
</form>
```

 

Todo campo input tiene que tener el atributo **name** que hace referencia a la información que enviaremos con el objetivo de poder identificar todos los inputs que mandemos dentro del formulario:

```html
<input name="nombre">
```

Para ayudar al usuario a entender la información que debe introducir en los campos tenemos el atributo **placeholder**

```html
<input name="nombre" placeholder="Introduce tu nombre..."/>
```

A la hora de validar la información que tienen que introducir el usuario en el input utilizaremos el atributo **type** que nos ayudará a controla el tipo de información que se introduce:

```html
<!-- Información de tipo texto -->
<input name="nombre" type="text" placeholder="Introduce tu nombre..."/>

<!-- Información de tipo numérico -->
<input name="edad" type="number" placeholder="Introduce tu edad..."/>

<!-- Información de tipo email -->
<input name="email" type="email" placeholder="Introduce tu email..."/>

<!-- Información de tipo password -->
<input name="email" type="password" placeholder="Introduce tu contraseña..."/>

<!-- Opción: Checkbox -->
<input name="opcion" type="checkbox">

<!-- Opción única: Radio -->
<input name="opcion" type="radio">

<!-- Archivos: File -->
<input name="opcion" type="file">
```

Por último, y cabe remarcarlo por separado, tenemos el tipo **submit** que nos va a permitir enviar toda la información del formulario

```html
<input type="submit">Enviar formulario
```

Cuando queremos enviar una observación o un campo de texto largo, utilizamos la etiqueta **textarea** en vez de input. Los atributos **cols** y **rows** nos permite cambiar el tamaño por defecto del textarea.

```html
<label>
    Observaciones
    <textarea placeholder="Observaciones" name="observaciones" cols="30" rows="10"></textarea>
</label>
```

A la hora de desarrollar, es muy frecuente que el input tipo submit sea un botón, utilizaremos esta etiqueta ya que nos dará muchas más posibilidades de personalización.

```html
<button type="submit">Enviar formulario</button>
```

En este atributo tenemos la propiedad **reset** que nos borrará la información de todo el formulario.

**VALIDACIÓN DE FORMULARIOS**

La validación de formularios en HTML5 nos va a permitir comprobar de forma nativa cada entrada de datos en base a unos atributos. No es personalizable así que nos tendremos que ajustar a las opciones que nos marcan los atributos.

 

Partiendo del siguiente formulario:

```html
<form method="post" action="/">
  <h3>Formulario registro gimnasio</h3>
  <fieldset>
		<legend>Datos personales</legend>
	  <label>
			Usuario:
			<input type="text" name="nombre" placeholder="Introduce tu nombre...">
		</label>
		<label>
			Apellidos:
			<input type="text" name="apellidos" placeholder="Introduce tus apellidos...">
		</label>
  </fieldset>
  <fieldset>
		<legend>Datos suscripción</legend>
	  <label>
			Dias que asistirás al gimnasio:
			<input type="number" name="dias" placeholder="Introducde el número de días...">
		</label>
		<label>
			Nick de usuario:
			<input type="text" name="nick" placeholder="Introduce tu nick para el gimnasio...">
		</label>
  </fieldset>
  <button type="submit">Registrarse</button>
</form>
```

 

Los tipos de validación básicos serían:

**TYPE**

Ya hemos ido utilizándolo a lo largo de los formularios. El tipo del input es la primera validación en función de si es texto, número, email, contraseña…

**REQUIRED**

Hace referencia a si un campo es obligatorio rellenarlo en el formulario. Utilizamos el atributo **required.**  No se podrá enviar la información del formulario hasta que el campo esté relleno.

 

```html
<form method="post" action="/">
  <h3>Formulario registro gimnasio</h3>
  <fieldset>
		<legend>Datos personales</legend>
	  <label>
			Usuario:
			<input type="text" name="nombre" placeholder="Introduce tu nombre..." required>
		</label>
		<label>
			Apellidos:
			<input type="text" name="apellidos" placeholder="Introduce tus apellidos..." required>
		</label>
  </fieldset>
  <fieldset>
		<legend>Datos suscripción</legend>
	  <label>
			Dias que asistirás al gimnasio:
			<input type="number" name="dias" placeholder="Introducde el número de días..." required>
		</label>
		<label>
			Nick de usuario:
			<input type="text" name="nick" placeholder="Introduce tu nick para el gimnasio...">
		</label>
  </fieldset>
  <button type="submit">Registrarse</button>
</form>
```

 

**MAXLENGTH / MINLENGHT**

Con estos atributos validaremos un número máximo o mínimo de caracteres. Con estos atributos podremos controlar el número de caracteres que queremos, ya sea una horquilla o un número exacto

 

```html
<form method="post" action="/">
  <h3>Formulario registro gimnasio</h3>
  <fieldset>
		<legend>Datos personales</legend>
	  <label>
			Usuario:
			<input type="text" name="nombre" placeholder="Introduce tu nombre..." maxlength="10" required>
		</label>
		<label>
			Apellidos:
			<input type="text" name="apellidos" placeholder="Introduce tus apellidos..." minlength="5" required>
		</label>
  </fieldset>
  <fieldset>
		<legend>Datos suscripción</legend>
	  <label>
			Dias que asistirás al gimnasio:
			<input type="number" name="dias" placeholder="Introducde el número de días..." required>
		</label>
		<label>
			Nick de usuario:
			<input type="text" name="nick" placeholder="Introduce tu nick para el gimnasio...">
		</label>
  </fieldset>
  <button type="submit">Registrarse</button>
</form>
```

 

**MIN/MAX**

De igual manera que en los atributos anteriores, min y max nos ayudarán a controlar los campos numéricos poniendo limitaciones.

 

```html
<form method="post" action="/">
  <h3>Formulario registro gimnasio</h3>
  <fieldset>
		<legend>Datos personales</legend>
	  <label>
			Usuario:
			<input type="text" name="nombre" placeholder="Introduce tu nombre..." maxlength="10" required>
		</label>
		<label>
			Apellidos:
			<input type="text" name="apellidos" placeholder="Introduce tus apellidos..." minlength="5" required>
		</label>
  </fieldset>
  <fieldset>
		<legend>Datos suscripción</legend>
	  <label>
			Dias que asistirás al gimnasio:
			<input type="number" name="dias" placeholder="Introducde el número de días..." max="7" min="1" required>
		</label>
		<label>
			Nick de usuario:
			<input type="text" name="nick" placeholder="Introduce tu nick para el gimnasio...">
		</label>
  </fieldset>
  <button type="submit">Registrarse</button>
</form>
```

 

**PATRÓN**

Este atributo nos permite validar el contenido de un input usando expresiones regulares, por ejemplo podríamos validar que un input solo contenga letras y números, nada de caracteres especiales

 

```html
<form method="post" action="/">
  <h3>Formulario registro gimnasio</h3>
  <fieldset>
		<legend>Datos personales</legend>
	  <label>
			Usuario:
			<input type="text" name="nombre" placeholder="Introduce tu nombre..." maxlength="10" required>
		</label>
		<label>
			Apellidos:
			<input type="text" name="apellidos" placeholder="Introduce tus apellidos..." minlength="5" required>
		</label>
  </fieldset>
  <fieldset>
		<legend>Datos suscripción</legend>
	  <label>
			Dias que asistirás al gimnasio:
			<input type="number" name="dias" placeholder="Introducde el número de días..." max="7" min="1" required>
		</label>
		<label>
			Nick de usuario:
			<input type="text" name="nick" placeholder="Introduce tu nick para el gimnasio..." pattern="**[A-Za-z0-9]"**>
		</label>
  </fieldset>
  <button type="submit">Registrarse</button>
</form>
```

 

Por último, la etiqueta **TITLE** dentro del input nos permitirá mostrar el aviso que queramos en cada input.
