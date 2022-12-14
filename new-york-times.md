Vamos ahora a practicar todo lo aprendido estructurando el documento HTML de la web del NYT. Es la siguiente:

[NewYorkTimes.pdf](recursos/NewYorkTimes.pdf)

El resultado final sería:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>New York Times</title>
</head>
<body>
    <header>
        <img width="600" src="./assets/logo.png" alt="logo NYT">
        <hr>
    </header>
    <main>
        <section>
            <article>
                <p>9 de septiembre de 2022</p>
                <div>
                    <h2>‘El puente de Londres ha caído’</h2>
                    <p>El final de la era de Isabel II, qué sigue para Carlos III y otras lecturas para el fin de semana.</p>
                    <p>Por ELDA CANTÚ</p>    
                </div>
                <img width="300" src="./assets/img-queen.webp">
            </article>
            <article>
                <p>9 de septiembre de 2022</p>
                <div>
                    <h2>‘No me interesa, quiero morir’: el viaje de un adolescente al lado oscuro de internet</h2>
                    <p>Mientras la ansiedad y la depresión se disparan entre los adolescentes, los investigadores se esfuerzan por comprender cómo afectan exactamente las redes sociales a la salud mental.</p>
                    <p>Por MATT RICHTEL</p> 
                    <a href="">Read in English</a>   
                </div>
                <img width="300" src="./assets/img-dark.webp">
            </article>
            <article>
                <p>9 de septiembre de 2022</p>
                <div>
                    <h2>Cómo China ha aumentado su influencia sobre los iPhone</h2>
                    <p>Apple quiere empezar a producir dispositivos en la India, pero el proceso de fabricación de su último teléfono, presentado el miércoles, muestra lo difícil que será el cambio.</p>
                    <p>Por TRIPP MICKLE</p> 
                    <a href="">Read in English</a>   
                </div>
                <img width="300" src="./assets/img-apple.webp">
            </article>
        </section>
    </main>
    <aside>
        <img src="./assets/anuncio1.jpg" alt="imagen publicitaria">
    </aside>
    <footer>
        <p>2022 The New York Times Company</p>
        <ul>
            <li><a href="">NYTCo</a></li>
            <li><a href="">Contact Us</a></li>
            <li><a href="">Accesibility</a></li>
            <li><a href="">Work with us</a></li>
            <li><a href="">Advertise</a></li>
        </ul>
    </footer>
</body>
</html>
```
