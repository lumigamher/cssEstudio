1. Siempre link en el html para carcar el css
2. los estilos se agregan con llaves 
.estilo {
    estilos a asignar al elemento 
}

3. para editar los estilos se nesecitan selectores 
    los selectores pueden ser_
    1. por id
        estos se llaman en el archivo css con #id_asignado

        de esta manera nos sercioramos de escojer el elemento que tiene 
        ese valor de id asignado dentro del html
    2  por class    
        para llamar por class se hace asi .class_asignada con el punto adelante
        y se separa con u espacio 

        tambien se pude nombrar la etiqueta.clase asi de esta manera
        div p {
            color: darkblue;
        }
    3. por *
        SIRVE PARA APLICAR PROPIEDADES A TODO EL ARCHIVO SIEMPRE Y CUANDO
        NO HAYAN SIDO MODIFICADAS

        * {
            SOLO CAMBIA LAS PROPIEDADES QUE 
            NO HAYAN SIDO TOCADAS
        }

4. para comentar se puede usar /*comentario*/    o varias lineas 

    /*aside
    asideasd
    asideasd
    asd*/

5. Elegir colores dentro de css:

    1. hexagesimal
        se escribe con #color

        con tres caracteres: 

            #000 negro
            #f00 rojo
            #0f0 verde
            #00f Azul

        con seis caracteres 

            de a dos caracteres por color
            permite una mayor cantidad de colores y variaciones 

            ej 
                #ff0000 rojo

    2. con RGB
        color: rgb(red, green, blue);
        color: rgb(000, 000, 000);

6. Bordes 

    border: 5px black solid;
    border: tamaño color estilo;

    tambien tiene porpiedades especificas 
    como:
        border-color: aquamarine;
        border-style: dashed;
        border-radius: 5px;
        border-width: 5px;

    Unidades de medida:
    hay muchas pero se usa px pixeles
    o rem es relativo al tamoño de la fuente
    del elemento raiz

    1 rem es aproximadamente 16px pero no siempre 

7. Fondos de los elementos 

    BACKGROUND

    background-color: rgba(0, 0, 0, 0.3); le asigna un color al Fondos
    opacity: 0.2; le da opacidad a todo el elemento 1 trasparente 0 full
    height: 400px;
    background-image: url(/storage/img/resumen-bombilla-creativa-sobre-fondo-azul-brillante-ia-generativa_188544-8090.avif);
    background-size: 200px 300px;
    background-repeat: repeat-y;
    background-position: center;

    o tambien se pueden agregar casi todas dentro de la general 
    asi:
        background: #f00 url(/storage/img/6d8841b6-9d24-457a-95c5-0d3de1d7bf5f.png) repeat-x center bottom;
    solo separandolas por un espacio
    EL size debe implementarse siempre despues de backgroud
    para que no sea ignorado

8. MARGIN y padding margenes afuera y adentro de los elementos 
    1. a.margenes afuera:

        margin: 15px 20px 25px 30px;
                top rigth bottom left
        
        b.espacio dentro del elemento 

        padding: 30px 25px 20px 15px;
                top rigth bottom left


        margin: 15px;

        con un valor toma todos los margenes iguales 
        con dos valores el primero es los verticales 
        y el segundo los horizontales 

9. overflow
    se utiliza para acomodar el contenido cuando este no cabe en su caja
    tiene varias opcioes para ocultar visibilizar escrolear que le agrega scrolñ para poder ver el elemento

    overflow: scroll; /hidden para ocultar /visible

10. outline
    se utiliza para agregar una linea afuera del borde 
    
    outline: 1px solid red;
            TAMAÑO/TIPO DE LINEA/COLOR   
     

11. TEXTO
    text-align: justify;

        para alinear justificar posicionar texto 
        con justify se justifica en el espacio que tiene disponible

    text-decoration: line-through;

        esto me agrega decoraciones como tachado negrilla etc
    
    text-shadow: 3px 4px 3px blue;

        esto agrega sobra siendo los valores en px los desplazamientos en los ejes 
        y el ultimo valor el color

12. FUENTES

    font-family: "Roboto", sans-serif;

    Propiedades para interactuar 

        le asigna una propiedad mientras no se haya pulsado el link
        a:link {
            color: yellow;
        }

        le asigna propiedasdes cuenado ya ha visitado el link
        a:visited {
            color: gray;
        }

        Le asigna una propiedad cuando pasa el mouse por ensima 
        a:hover {
            color: blueviolet;
        }

        a:active {
            color: red;
        }

13. LISTAS

    Las comunes son list-style que permite cambiar las viñetas 
    el padding igual que entodas cambia el margen hacia adentro 
    se le pueden agregar atributos de color backgrund etc

    ul {
        background-color: cadetblue;
        list-style: none;
        padding-left: 0%;
        /* list-style-position: inside; */

    }

14. TABLAS


        table {
            width: 100%;
            border-collapse: collapse; <-- esta hace que se colapcsen los bordes y se vea todo encerrado

        }
        th, td {
            border: solid 1px black; le asigna borses a cada elemento arriba los une con collapse
            text-align: left; alinea a la izquierda
        }

        este selector me sirve para escojer valores en especifico
        en este caso coje las filas impares con el even 
        tr:nth-child(even) {
            background-color: #eee;
        }
        
        el hover me permite agregar funciones cuando pase el cursor por cada fila 
        o columba segun ponga la etiqueta esta vez es tr de fila 
        th de colmna

        tr:hover {
            background-color: aquamarine;
            cursor: pointer;
        }

15. display

span {
    display: block; /*hace salto le asigna un bloque de pantalla*/
    max-width: 300px;
    background-color: aqua;
}

.inline {
    display: inline; /*los pone sobre la misma linea*/  
}

16. position 
    position: relative; 
    es una posicion que es relativa a donde debiera estar posicionado
    este elemento

    position: fixed;
    le indica que debe tener una posicion pero con respecto 
    a lo que se ve en el explorador 
    se queda fijo en la pantalla asi escrolleemos

    position: absolute;
    se posiciona relativo con el elemento padre mas cercano a el 
    por defecto es body si no hay otro

    position: sticky;

    es una mescla entre relative y fixed

17. float inline-blok etc
    .left {
        float: left;
        width: 400px;
    }
    .rigth {
        float: right;
    }

    .container {
        height: 200px;
    }

    .column {
        width: 33%;
    }

    .inline-block {
        display: inline-block; esto ayuda para que le aportemos propiedades de altura o ancho
        height: 55px;
        background-color: red;
    }

    .center {
        text-align: center;
        
        width: 200px;
        margin: 0 auto;
        background-color: red;
    }





    







      








