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
    1. margenes afuera:

        margin: 15px 20px 25px 30px;
                top rigth bottom left

        margin: 15px;

        con un valor toma todos los margenes iguales 
        con dos valores el primero es los verticales 
        y el segundo los horizontales 


    2. espacio dentro del elemento 

        padding: 30px 25px 20px 15px;
                top rigth bottom left









