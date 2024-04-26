# Docker_micro_app
An app composed of 4 microservices that communicate with each other, built with Python + Flask, and where data will be stored in PostgreSQL, managed with the Docker-compose tool


# Microservicios Dockerzados

## Description

La aplicación implementa una arquitectura de microservicios que se comunican entre sí mediante una API RESTful. Cada servicio está aislado en un contenedor Docker.

Es una aplicación web construida en Python utilizando el framework Flask. Se compone de cuatro servicios que se comunican entre sí a través de una API, cada uno de ellos alojado en un contenedor Docker. La aplicación incluye un servicio de base de datos PostgreSQL, un generador de datos falsos, un servicio web que renderiza los templates de HTML y Bootstrap, y un API que comunica todos estos servicios.

## Estructura del proyecto

El proyecto se compone de la siguiente estructura:

- **api**: carpeta que contiene el código fuente y los archivos necesarios para ejecutar el servicio de la API. Esta carpeta contiene el archivo **Dockerfile** que define cómo se construirá el contenedor de la API. Además, se incluye el archivo api-service.py que contiene el código fuente del servicio de la API y **requirements.txt** que especifica las dependencias que necesita el servicio.

- **database_postgresql**: carpeta que contiene los archivos necesarios para ejecutar el servicio de la base de datos PostgreSQL. Esta carpeta contiene el archivo database.env que define las variables de entorno necesarias para configurar el servicio de la base de datos y el archivo **init.sql** que contiene el script SQL para inicializar la base de datos.

- **faker**: carpeta que contiene el código fuente y los archivos necesarios para ejecutar el servicio del generador de datos falsos. Esta carpeta contiene el archivo Dockerfile que define cómo se construirá el contenedor del generador de datos. Además, se incluye el archivo **faker-service.py** que contiene el código fuente del servicio del generador de datos y requirements.txt que especifica las dependencias que necesita el servicio.

- **web**: carpeta que contiene el código fuente y los archivos necesarios para ejecutar el servicio web que renderiza los templates de HTML y Bootstrap. Esta carpeta contiene el archivo Dockerfile que define cómo se construirá el contenedor del servicio web. Además, se incluye el archivo **web-service.py** que contiene el código fuente del servicio web y requirements.txt que especifica las dependencias que necesita el servicio. La carpeta también contiene una subcarpeta llamada templates que contiene los templates de HTML y los archivos CSS y JavaScript necesarios para renderizar la página web.

- **docker-compose.yml**: archivo que define todos los servicios que se deben ejecutar y cómo deben comunicarse entre sí. En este archivo se especifica cómo se deben configurar los contenedores y cómo deben conectarse a la red.

## Cómo ejecutar el proyecto

Para ejecutar este proyecto, es necesario tener instalado Docker y Docker-compose en su sistema. Una vez que haya clonado o descargado el repositorio, siga estos pasos:

1. Abra una terminal en la raíz del proyecto.
2. Ejecute el comando docker-compose up.
3. Espere a que Docker descargue e instale todas las dependencias necesarias y los contenedores se inicien.
4. Una vez que todos los contenedores estén en funcionamiento, puede acceder a la aplicación a través de un navegador web en **http://localhost:5002**.