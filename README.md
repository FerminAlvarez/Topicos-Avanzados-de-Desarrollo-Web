# Topicos Avanzados de Desarrollo Web

# Introducción
El desarrollo web ha ido evolucionando ...

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

# Docker Compose

# RabbitMQ

# Serverless

# Page Rendering y JAMStack

# Entrega e Integración Continua
