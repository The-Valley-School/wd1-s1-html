En este video vamos a ver primero cómo incluir imágenes, vídeos y audio en nuestro HTML y después como incrustar contenido que nos puede ser de gran ayuda.

**CONTENIDO MULTIMEDIA**

**IMÁGENES**

La etiqueta img nos va a permitir introducir imágenes dentro de nuestra página web. Al igual que otras etiquetas esta no tendría cierre. 

Para trabajar sobre esta etiqueta tenemos una serie de atributos. Los más importantes:

- **src**  donde introducimos la url de la imagen

  

```html
<img src="gatito.jpg">
```

   

- **width y height** que utilizamos para cambiar el tamaño del ancho y la altura en píxeles. Siempre es mejor incluir una clase para tratar el tamaño de las imágenes mediante CSS.

 

```html
<img src="gatito.jpg" width="100" height="100">
```

  

- **alt** es un atributo que nos vale para mostrar un texto en caso de que no se visualice correctamente la imagen, ya sea porque tiene un formato no soportado o porque no hemos introducido bien la URL.

 

```html
<img src="gatito.jpg" alt="Imagen de un gatito">
```

  

- **longdesc** si queremos mostrar una descripción detallada de la imagen complementando al texto de **alt**

 

```html
<img src="gatito.jpg" alt="Imagen de un gatito" longdesc="Descripción de lo que hace el gato">
```

  

- **srcset** nos permite optimizar el consumo de recursos y adaptarnos a las web responsive

 

```html
<img src="gatito.jpg" srcset="img_small.jpg 300w, img_medium.jpg 1200w, img_large.jpg 1800w">
```

 

- **sizes** nos permite ajustar aún más estas imágenes al tamaño de pantalla.

 

```html
<img src="gatito.jpg" srcset="img_small.jpg 300w, img_medium.jpg 1200w, 
img_large.jpg 1800w" sizes="(max-width: 320px) 300px, (max-width: 1200px) 
1200px, 1800px" alt="la imagen de mi producto">
```

**VIDEO Y AUDIO**

Al igual que la etiqueta img nos permitía incluir imágenes dentro del documento HTML, tenemos la etiqueta video que nos permite incluir vídeos dentro de nuestro HTML

 

```html
<video></video>
```

 

Esta etiqueta tiene una serie de atributos que nos ayudan a trabajar con ella

- **src** para incluir la URL del vídeo.

 

```html
<video src="video1.mp4"></video>
```

 

- **controls** es de tipo boolean y la utilizaremos si queremos incluir controles de reproducción de vídeo

 

```html
<video src="video1.mp4" controls></video>
```

 

- **autoplay** es de tipo boolean y la utilizaremos para indicar que inicie a reproducirse cuando cargue el vídeo

 

```html
<video src="video1.mp4" autoplay></video>
```

  

- **muted** es de tipo boolean y la utilizaremos para establecer el vídeo sin sonido

 

```html
<video src="video1.mp4" muted></video>
```

  

- **loop** es de tipo boolean e iniciará de nuevo el vídeo cuando se termina

 

```html
<video src="video1.mp4" loop></video>
```

 

- **width y height** nos permiten también cambiar el tamaño del video.

 

```html
<video src="video1.mp4" height="100" width="100"></video>
```

 

De la misma manera, la etiqueta **audio** nos permite incluir audio en nuestra página web.

 

```html
<audio></audio>
```

 

Esta etiqueta también tiene los atributos src, autoplay, loop, muted y controls, que funcionan de la misma manera que la etiqueta video

**RUTAS**

Tras haber trabajado con estas etiquetas y con los enlaces en el vídeo anterior, vemos que es necesario saber manejar rutas para poder incluirlas dentro de nuestro HTML.

Ya no solo enlaces, imágenes, video y audio, si on también los diferentes ficheros de css y Javascript que vamos incluyendo en nuestro proyecto.

**RUTAS ABSOLUTAS**

Son rutas que no dependen del contexto en el que estemos navegando y siempre apuntan al mismo sitio, da igual desde donde se las llame.

La estructura general de este tipo de rutas es:

  

```html
PROTOCOLO | PUERTO | DOMINIO | UBICACIÓN
```

 

Un ejemplo sería:

   

```html
https://thevalley.es/formacion/
```

  

Podríamos incluir una imagen de google también como ruta absoluta.

Este tipo de rutas son interesantes para enlaces fuera de nuestro dominio, a la hora de trabajar bajo un mismo dominio tiene sentido usar rutas relativas

**RUTAS RELATIVAS**

Nos sirven para referencias elementos que encontramos bajo un mismo dominio, es decir, sobre la página HTML en la que no s encontramos. Lo bueno, que no dependemos de donde se despliegue la página.

Tenemos de varios tipos

- **Rutas /**
    
    Son las que generaremos a partir del dominio en el que nos encontramos. Por ejemplo: 
    

   

```html
<img src="/imagen.jpg">
```

  

- **Rutas ./**
    
    Son las que generaremos a partir del punto en el que nos encontramos. Esta imagen estaría a la misma altura que mi documento html
    

   

```html
<img src="./imagen.jpg">
```

  

- **Rutas ../**
    
    Son las que generaremos a partir del anterior punto en el que nos encontramos, es decir, a partir de la carpeta que contiene el fichero html
    

   

```html
<img src="../imagen.jpg">
```

  

- **No indicando nada**
    
    En caso de no indicar ningún comienzo, empezaríamos desde el punto en el que nos encontramos, a la altura del documento que tenemos.
    

   

```html
<img src="imagen.jpg">
```

  

**CONTENIDO INCRUSTADO**

Para finalizar con el video, vamos a ver una etiqueta que nos van a ayudar a incrustar contenido en nuestro documento, más allá de las que ya hemos visto de contenido multimedia.

**IFRAME**

La etiqueta iframe nos va a permitir incrustar un documento web dentro de la página. Esta página tendrá sus propios estilos, contenidos…

A continuación indicamos los atributos más importantes:

- **src** indica la URL de la página
- **width y height** permiten modificar el ancho y el alto donde mostramos la página
- **allowfullscreen** es de tipo booleano y activa en caso de ser posible el modo pantalla completa