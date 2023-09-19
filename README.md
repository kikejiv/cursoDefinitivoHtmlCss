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

## *Anatomia de una regla de CSS*
a los estilos que se implementan se le llaman reglas css se componen de 
1. Selector: es decirle a css que elemento quieres modificar
2. Propiedad: es el estilo que se le va a aplicar al selector
3. El valor de la propiedad: es lo que se espera que se vaya a aplicar y finalizamos con punto y coma
    p {
        color: red;
    }

## *Pseudoclases y Pseudoelementos*
Una [**pseudoclase**](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes) CSS es una palabra clave que se añade a los selectores y que especifica un estado especial del elemento seleccionado. Por ejemplo, a:hover aplicará un estilo cuando el usuario en conclucion, esta define el estilo de un estado espacial de un elemento

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

[**los pseudoelementos**](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-elements)  permiten añadir estilos a una parte concreta del documento. Por ejemplo, el pseudoelemento a::after selecciona solo la primera línea del elemento especificado por el selector.define el estilo de un parte especifica de un elemento

    .main-nav__item a::after {
        content: " | ";
    }

## *Modelo de caja*
son contenedores que pueden llevar contenido y pueden llevar ciertos estilos y tiene las sigientes propiedades
1. margin. puede ser un espacio externo de la caja hacia afuera
2. border. es la linea qu va a definir cada uno de los elementos por defaul viene transparente y se le puede poner un color y un ancho
3. padding. es un espacio interno de lacaja hacia adentro y ayuda para posisionar el contenido
4. content. puede ser el texto las imagenes o el video
   
tenemos unas clases las cuales son width que equivale al largo del contenido, el heigth es el alto ademas se puede pósisionar con top (arriba), bottom(abajo), left(ala izquierda), right(a la derecha)

## *Herencia*
es el codigo css que se le pasa de un padre a un hijo, cuando toma los estilos de otra etiqueta

**Herencia y sus valores:**
1. Inherit. Este es un valor por medio de una keyword que especifica que, a la propiedad que se la apliquemos debe de heredar los valores de su elemento padre. Podemos decir que la palabra Inherit significa “Usa el valor de mi padre”, si el elemento padre no tiene definido dicho valor el navegador seguirá el DOM hasta que encuentre un elemento superior que lo contenga, y en ultima instancia de no tenerlo ningún elemento superior se aplicara el valor por defecto.

2. Initial. Este valor pertenece a la especificación CSS3 y cuando aplicamos a una propiedad el valor initial estamos dando el valor inicial y predefinido por el navegador en cuestión.

3. Upset. Este valor unset es una combinación entre inherit y initial, cuando utilizamos este valor en una propiedad esta tratara de heredar el valor de su elemento padre si este esta disponible, de no ser así este valor colocará el valor de la propiedad en su valor inicial, como si usáramos inherit e initial juntos.

## Como controla el orden al declarar CSS
1. Importancia: es uno de los conceptos  mas importantes si dos declaraciones tiene la mis ma importancia, la especificidad decidira cual regla se le debe aplicar cuando se carga un proyecto primero se  implementan los estilos por defecto del navegador, luego se cargan los estilo que nosotros trabajamos y por ultiom se cargaran los estilos que contengan un important en nuestra hoja de estilo

2. Especificidad: !important es el mas importante y se aplicaran de primero, inline styles son los estilos que se enbeben en las etiquetas html, despues entran los estilos que se apliquen a los id(#), luego a las clases(.)y por ultimo a los selectores como etiquetas html

3. Orden en las fuentes. es la forma en la que se mandan a llamar los estilos  siempre se enpezara de la primera linea hasta abajo

utilizar tantos id no es buena practica lo mejor es utilizar las clases y los selectores que ya conocemos, debemos quitar los id y remplazarlos por las clasesporque esto nos puede ocasionar muchos problemas despues, se llama la clase de forma directa y se ignora el id  antes #main-nav   ahora .nav ej:  #main-nav li    .nav li

## Los combinadores
permiten crear combinaciones multiples de selectores y crear una payor specificidad entre los cuales hay 4

1. hermano adyacente o cercanos: se separa por el signo + (div + p {... }) estiliza todas las p cercanas al div ej:
   ``` 
        h2 + p {
            color: red
        }
        <div>
            <h2>Soy un titulo</h2>
            <p>soy un parrafo</p>
            <h2>Soy otro titulo</h2>
            <p>soy otro parrafo</p>
            <h3>Soy sub titulo</h3>
            <p>soy un parrafo</p>        
        </div>
    solo estilizara la etiqueta p que esten cerca al h2
2. hermanno general: nos permite estilizar todas las etiquetas hernamo  se separa por el signo ~ (div ~ p {... }) ej:
    ``` 
        h2 ~ p {
            color: yellow
        }
        <div>
            <h2>Soy un titulo</h2>
            <p>soy un parrafo</p>
            <h2>Soy otro titulo</h2>
            <h3>Soy sub titulo</h3>
            <p>soy un parrafo</p>        
        </div>
    estilizara todas las etiquetas p debido a que son hermanos
3. hijos: agrega los estilos a los hijos directos se separa por el signo > (div > p {... }) ej:
    ``` 
        div > p {
            color: yellow
        }
        <div>
            <article>
                <p>soy un parrafo</p>
            </article>
            <article>
                <p>soy un parrafo</p>
            </article>    
            <section>
                <div>
                    <p>soy un parrafo</p>
                </div>
            </section>  
            <p>soy un parrafo</p>    
        </div>
    estilizara solo la tercera y cuarta etiquetas p debido a que son hijas directas del div
4. descendiente: todas las etiquetas que eten dentro de un contenedor (div p { }) ej
    ``` 
        div p {
            color: blue
        }
        <div>
            <article>
                <p>soy un parrafo</p>
            </article>
            <article>
                <p>soy un parrafo</p>
            </article>    
            <section>
                <div>
                    <p>soy un parrafo</p>
                </div>
            </section>  
            <p>soy un parrafo</p>    
        </div>
     estilizara todas las etiquetas p debido a que son hijos de la etiqueta global div

## ***Medidas***
hay dos parametros las cuales son medidas relativas y medidas absoluta
 1. **medidas absolutas** utilizamos pixeles vamos a poner el tamaño del  fuente utilizamos el width, el heigth y esta medida no va a cambiar sin importar el tamaño de la pantalla donde estemos viendo el proyecto
 2. **medidas relativa**  el tamaño varia mucho dependiendo el dispositivo en donde se este viendo y no solo se usa el porcentaje tambien se utiliza el em que es (elemento), el rem (root en elemento), max-width / max-height, min-width / min-height, vw (viewport width) vh (viewport height) 
   **el em** depende de la dimension marcada delpadre directo que puede se diferente
   **el rem** se utiliza como si fueran pixeles 1rem = 16px y siempre va ha hacer referencia a la etiqueta root del proyecto
   **el vw y vh** ayuda a darle ciertas dimensiones a contenedores padres 
   **max-width / max-height, min-width / min-height** delimita el crecimiento del contenedor ayuda mucho para cuando el texto se salga del contenedor **(overflow)** 

## ***Position***
es la forma en que posicionamos las etiquetas, las cajaas y los contenedores tenemos diferntes position static, absolute, relative, fixed, sticky
- static. es la que viene por defecto en las etiquetas y se queda en donde se pone por esocuando se hace scroll no se mueve
- absolute 