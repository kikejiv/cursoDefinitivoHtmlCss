# cursoDefinitivoHtmlCss

## **Etiquetas de formatos multimedia**

### Etiquetas de imagenes
 #### *Como utilizar la etiqueta Img y figure*
 la etiqueta imge tiene dos atributos src="" alt=""  src es para decir donde se encuentra la imagen(se puede sacar de alguna carpera o de alguna url de internet, alt es para dar la descripcion de la imagen y ayuda para el tema de accesibilidad puede decir la descripcion en caso que no se vea la imagen)
 la etiqueta figure nos ayuda a generar un contenedor para la imagen
 hay una etiqueta nueva que se llama figcaption y da una descripcion visual de la imagen
 #### *Tipos de imagenes*
 existen dos tipos de imagenes, lossy vs lossless (con perdida / sin perdida ), las imagines que tienen perdida por lo general son mucho mas pequeñas que las imagenes que tienen perdida y pueden cargar mucho mas rapido en el  navegador, si hay que escoger imagenes que pueden perder calidad  formatos Lossless (gif - png 8 tiene un uso de 256 colores - se utiliza para logos - png 24 tiene mas de 256 colores - svg es un formato muy ligiro y se utiliza mucho en iconos)  formatos Lossy (jpg/jpge tiene gama de colores ilimitada)
 ![Tabla de imagenes](tabla de imagenes.JPG)

 #### *Optimizando imagenes*
 el tamaño optimo en promedio debe pesa 70kb Herramientas para optimizar imágenes [Tiny PNG](https://tinypng.com/): Comprime el tamaño de una imagen, para hacerla más ligera. [Verefix](https://www.verexif.com/): Elimina los metadatos de una imagen, para reducir su tamaño. [Convertio](https://convertio.co/es) convierte jpg, png a svg (esta pagina es muy buena puede convertir de todo a otros formatos es gratis, chequenla y comenten que les parecio ) 
 url para descargar imagenes Pexels, Pixabay, Freerange, Realistic Shots, PicJumbo, Magdeleine, Creativecommons, Freejpg

# Formularios

#### *Input type*
El elemento HTML [input](https://developer.mozilla.org/es/docs/Web/HTML/Element/input) se usa para crear controles interactivos para formularios basados en la web con el fin de recibir datos del usuario
[tipos de input](https://www.w3schools.com/html/html_form_input_types.asp)


# ***CSS***
css es el documento para aplicar los estilos visual en forma de cascada [Css](https://htmlcheatsheet.com/css/)
para ligar css al proyecto en un archivo html se utiliza 3 formas
1. la etiqueta link **(link rel="stylesheet" href="style.css")** para eso debo crear el archivo css es la mejor manera
2. con la etiqueta style y denrto de ella se agrega el codigo css en el mismo archivo html, no es la mejor practica porque si hay muchas lineas de codigo se demorara mucho en cargar la pagina
3. es como atributo a la etiqueta html ej (p style="color: red">Soy un texto</p) y a este se le llama estilo enbebido o inyectado

las etiquetas las mandamos a llamar  en nuestro archivo .css de tres maneras o selectores
1. por el elemento quiere decir por la etiqueta a la que vamos a estilizar ej: 
   ```
   <p>

   p {
       color: blue;
       font-size: 30 px;
   } 
2. por la clase es cuando a la etiqueta se le agrega el atributo class y se le da un nombre a la clase ej:
   ```
   <p class="parrafo">Soy un texto</p>

   .parrafo {
       color:red;
   }
3. y el otro selector el por id y se llama con un numeral ej:
   ```
    <p id="texto">Soy un texto</p>

    #texto {
        color: yellow;
        font-size: 20px;
    }

## *Pseudoclases y Pseudoelementos*
Una [**pseudoclase**](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes) CSS es una palabra clave que se añade a los selectores y que especifica un estado especial del elemento seleccionado. Por ejemplo, :hover aplicará un estilo cuando el usuario en conclucion, esta define el estilo de un estado espacial de un elemento

Html
     <header>
            <nav>
                <ul class="main-nav">
                    <li class="main-nav__item"><a href="">Home</a></li>
                    <li class="main-nav__item"><a href="">Cursos</a></li>
                    <li class="main-nav__item"><a href="">Instructores</a></li>
                    <li class="main-nav__item"><a href="">Blog</a></li>
                </ul>
            </nav>
    </header> 
Css
    .main-nav {
        margin-top: 10px;
        list-style: none;
        padding: 0;
        background-color: rgb(130, 70, 186);    
    }

        .main-nav__item {
            display: inline-block;
        }

        .main-nav__item a {
            color: white;
            padding: 5px;
            text-decoration: none;
        }

        .main-nav__item a:hover {
            color:rgb(52, 199, 225);
        }

   

[**los pseudoelementos**](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-elements)  permiten añadir estilos a una parte concreta del documento. Por ejemplo, el pseudoelemento ::first-line selecciona solo la primera línea del elemento especificado por el selector.define el estilo de un parte especifica de un elemento