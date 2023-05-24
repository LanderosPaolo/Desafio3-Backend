# Acceso a Base de Datos con Node (Parte I)
Este es un repositorio de ejemplo que contiene un servidor de API REST desarrollado con Node.js y Express, y utiliza una base de datos PostgreSQL para almacenar y recuperar publicaciones.

## Requisitos

    Node.js
    PostgreSQL
    Express Js
 
## Base de datos
  ### Creando base de datos
    CREATE DATABASE likeme;
  ### Ingresando a base de datos
    \c likeme
  ### Creando tabla
    CREATE TABLE posts (id SERIAL, titulo VARCHAR(25), img VARCHAR(1000), descripcion VARCHAR(255), likes INT);
    
## Configura la base de datos:
   - Asegúrate de tener PostgreSQL instalado y en funcionamiento.
   - Crea una base de datos llamada likeme en PostgreSQL.
   - Abre el archivo consultas.js y modifica los valores 
      (host, user, password y database) en el objeto pool de acuerdo a tu configuración de PostgreSQL.
      
## Uso

### Obtener todas las publicaciones

#### Este endpoint devuelve todas las publicaciones almacenadas en la base de datos.

    GET /posts


### Agregar una publicación

    POST /posts

#### Este endpoint permite agregar una nueva publicación. Debes enviar los siguientes datos en el cuerpo de la solicitud en formato JSON:

    {
    "titulo": "Título de la publicación",
    "url": "URL de la publicación",
    "descripcion": "Descripción de la publicación"
    }
    
## Inicia el servidor
    npm run dev

