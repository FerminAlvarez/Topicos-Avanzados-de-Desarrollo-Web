# Topicos Avanzados de Desarrollo Web

# Introducción
En este repositorio se hará un resumen de los temas y sus correspondientes actividades que desarrollamos durante la cursada de Topicos Avanzados del Desarrollo Web - Universidad Nacional del Sur - 2022

# Tabla de contenidos
- [GIT](#git)
- [NoSQL](#nosql)
- [GraphQL](#graphql)
- [Micro-Frontends](#micro-frontends)
- [Microservicios y escalabilidad](#microservicios-y-escalabilidad)
- [Docker](#docker)
- [Docker Compose](#docker-compose)
- [RabbitMQ](#rabbitmq)
- [Serverless](#serverless)
- [Page Rendering y JAMStack](#page-rendering-y-jamstack)
- [Entrega e Integración Continua](#entrega-e-integración-continua)

# GIT

## Vídeo Introductorio a GIT
[![Watch the video](https://img.youtube.com/vi/Ip1CTrJ4o_U/maxresdefault.jpg)](https://www.youtube.com/watch?v=Ip1CTrJ4o_U)

## Actividades

### GIT y GitHub
 - Se creó una organización con varios participantes de la catedra.
 - Se analizaron los distintos workflows y se optó por una branch por equipo.
 - Cada equipo implementó distintas funciones y se pushearon
 - Se realizaron Pull-Requests y se aprobaron/rechazaron
 - Se provocaron conflictos con el fin de realizar merges
 - Se vió la diferencia entre rebase y merge

# NoSQL

## Vídeo Introductorio a Bases de Datos NoSQL
[![Watch the video](https://img.youtube.com/vi/mgfRFhiqhTQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=mgfRFhiqhTQ)

## Actividades

### MongoDB
Partiendo de una [base de datos MongoDB sobre películas](https://raw.githubusercontent.com/FerminAlvarez/MongoDB-JS/main/movies.json), y una aplicacion inicial en Express que tiene una busqueda hardcodeada por titulo de película se pide:
 - Arreglar la busqueda para poder buscar por algún término indicado por el usuario. 
    - Para buscar por término, se debe crear un index en la base de datos que considere tanto al título como la trama y los nombres de los actores de las películas.
 - De cada película encontrada mostrar su título, año de estreno, rating de IMDB, Tomatoes y Metacritic. Buscar una vista linda para mostrar todos los datos
 - Agregar un boton adicional que realice una busqueda especifica hardcodeada. Buscar que sea lo mas complicada posible, combinando varios filtros.
 - Agregar un boton que obtenga 5 peliculas random de la base de datos, y agregue una nueva película en la base de datos que combine datos obtenidos de cada una de ellas.
    - Para obtener 5 peliculas random, se debe crear un Agregation que tenga un Sample de 5.
 - Crear una Agregation
 
---

### Firebase

Crear una base de datos en Firebase, y se realizar una app en Express que obtenga todas las películas cargadas en la base de datos. Para esto debe crearse una cuenta en Firebase, crear la base de datos y cargar datos en la base de datos. Luego se debe crear una aplicacion express, instalar las dependencias de firebase y ver como conectarse a la base de datos creada, y obtener datos de la misma para mostrarlos.

# GraphQL

## Vídeo introductorio a Bases de Datos GraphQL
[![Watch the video](https://i3.ytimg.com/vi/woEdVpoNUkk/maxresdefault.jpg)](https://www.youtube.com/watch?v=woEdVpoNUkk)

## Actividades

### GraphQL
---
Partiendo de una [API GraphQL de Star Wars](https://graphql.org/swapi-graphql) se solicitaron las consultas:
 - Listar las dos últimas películas registradas en la base de datos
 - Listar todos los planetas y las películas en las que aparecen.
 - Listar los nombres y el lugar de nacimiento de las primeras 4 personas de la base de datos.
 - El color de ojos de Obi-Wan Kenobi
 - Listar todas las películas y las razas que figuran en cada una de ellas indicando además un personaje de cada raza.
 - Listar todos los vehículos de Luke Skywalker y las películas en las que aparecen esos vehículos.
 
---
Partiendo de una [API GraphQL de Paises](https://countries.trevorblades.com/) se realizaron diversas consultas
 - Obtener los continentes con sus paises en los que se hable español.
---
Partiendo de una [API GraphQL de Clima](https://graphql-weather-api.herokuapp.com/) se solicitaron las consultas:
 - Obtener el clima de Paris en tiempo real en diferentes unidades.


# Micro-Frontends

## Vídeo introductorio a Micro-Frontends
[![Watch the video](https://i3.ytimg.com/vi/h3ukjSRw53M/maxresdefault.jpg)](https://www.youtube.com/watch?v=h3ukjSRw53M)

## Actividades
Creamos una aplicación React que contiene unicamente un Componente con una Frase de los simpsons, y mediante la utilizacion de un proxy invertido, en este caso Ngrok, enviamos el link de cada microfrontend al profesor, que hizo otra aplicación react que utilizaba cada componente entregado por los alumnos como un micro-frontend y los mostraba todos juntos. 

# Microservicios y Escalabilidad

## Vídeo introductorio a Microservicios y escalabilidad
[![Watch the video](https://i3.ytimg.com/vi/w0L6ify1v8c/maxresdefault.jpg)](https://www.youtube.com/watch?v=w0L6ify1v8c)

## Actividades
Se dividieron los alumnos en grupos, y cada uno fue encargado de realizar un microservicio diferente en express para intentar hacer una aplicación React que imite el home page de Netflix, algunos hicieron un microservicio para obtener las peliculas más populares, otros hicieron un microservicio para recomendar peliculas teniendo en cuenta las últimas visualizaciones, y para esto era libre consumir cualquier API, por ejemplo la de Open Movie Database o The Movie Database.
Estos microservicios volvimos a desplegarlos localmente y compartimos el puerto generado por Ngrok para que el profesor pueda consumirlos.

# Docker

## Vídeo introductorio a Docker
[![Watch the video](https://i3.ytimg.com/vi/8cn0nRRWXAw/maxresdefault.jpg)](https://www.youtube.com/watch?v=8cn0nRRWXAw)

## Actividades
Para comprender mejor como funcionan las imagenes de Docker y los contenedores, nos descargamos Docker Desktop, y luego realizamos dos actividades:
 - La primer tarea fue un poco más básica para familiarizarnos un poco con los Dockerfiles. Realizamos una aplicación básica en express cuyo funcionamiento no era lo importante para la tarea. Luego creamos la imagen utilizando docker build, y creamos el contenedor y lo probamos utilizando docker run.
 - Una vez familiarizados con el funcionamiento básico de docker creamos otra aplicación en express, que se conecta a una base de datos local en MongoDB y hace GETs para extraer información de la base de datos. Para esta nueva aplicación volvimos a crear la imagen y el contenedor correspondientes y lo probamos.
 
Además de estas actividades, jugamos un poco con DockerHub, primero hicimos pull de imagenes como la de MongoDB y corroboramos que funcionase, y luego nos creamos una cuenta y aprendimos como es el funcionamiento para poder subir tus imagenes locales al repositorio de DockerHub.

# Docker Compose

## Vídeo introductorio a Docker Compose
[![Watch the video](https://i3.ytimg.com/vi/L0klOFW187s/maxresdefault.jpg)](https://www.youtube.com/watch?v=L0klOFW187s)

## Actividades
Habiendo jugado previamente con la creación de imagenes y contenedores en el anterior módulo, estabamos listos para aprender sobre el funcionamiento de Docker Compose. Si bien habíamos aprendido cómo crear imagenes para aplicaciones y hacer que estas corran en un contenedor en determinado puerto, el verdadero jugo que tiene el utilizar herramientas como docker es el de poder "juntar" o "ensamblar" microservicios, pero sin tener que hardcodear los puertos en los que estos corren, ya que es una solución poco elegante. Para esto utilizamos el Docker Compose, un archivo YAML que nos permite realizar este tipo de configuraciones.  
Puntualmente, la actividad que realizamos fue la siguiente:
Se nos entrego un código en React que consumía 3 microservicios, uno en PHP, otro en express y otro en Python, que lo que hacían es generar numeros random del 0 al 99999, y la aplicación React los mostraba, y variaba el color dependiendo al microservicio al que se lo hubiese pedido, actualizando el número cada 3 segundos. Este código tenía en la aplicación React los puertos de los microservicios hardcodeados, por lo que nuestra tarea consistia en: 
 - Generar el Dockerfile para cada microservicio y para la aplicación en React.
 - Definir el docker-compose que permita ejecutar toda la aplicación en conjunto.
 - Configurar correctamente el docker-compose para que puedan configurarse los puertos y evitar hardcodearlos en el código.
 - Replicar alguno de los microservicios, ejecutando una misma imagen en contenedores diferentes.

# RabbitMQ

## Vídeo introductorio a RabbitMQ
[![Watch the video](https://i3.ytimg.com/vi/LYr3X4agbZI/maxresdefault.jpg)](https://www.youtube.com/watch?v=LYr3X4agbZI)

## Actividades


# Serverless
## Vídeo introductorio a Serverless
[![Watch the video](https://i3.ytimg.com/vi/ad8BzihRhYQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=ad8BzihRhYQ)

## Actividades
Haciendo uso de un código simple que nos fue brindado y de MongoDB Atlas 
- Crear una función Atlas que sólo imprima "Hola Serverless", inspirado el código mencionado anteriormente. Integrarlo en la app.
- Crear un trigger, que se active cada vez que se agrega un comentario en la colección "sample_mflix", y cargue en una colección nueva "avisos", un documento con el nombre de la persona que agrega el comentario. Probarlo agregando a mano en Atlas comentarios a esa colección. Debería agregar registros a "avisos" automaicamente.
- Crear una función que te muestre la ultima persona que hizo un comentario e integrarlo a la aplicación.

# Page Rendering y JAMStack
## Vídeo introductorio a Page Rendering y JAMStack
[![Watch the video](https://i3.ytimg.com/vi/VCdVV8KwuTc/maxresdefault.jpg)](https://www.youtube.com/watch?v=VCdVV8KwuTc)

## Actividades

# Entrega e Integración Continua
## Vídeo introductorio a Page Rendering y JAMStack
[![Watch the video](https://i3.ytimg.com/vi/Hj6qUv-T1qE/maxresdefault.jpg)](https://www.youtube.com/watch?v=Hj6qUv-T1qE)

## Actividades
