Descripción general:
Este proyecto es una aplicación en Java que permite gestionar un catálogo de películas utilizando el patrón Modelo – Vista – Controlador (MVC) y almacenamiento persistente en un archivo CSV. El sistema permite listar películas y agregar nuevas, guardándolas de forma permanente en un archivo externo.

Caracteristicas principales:

Gestión de películas (listar y agregar)

Persistencia mediante archivo CSV

Arquitectura basada en MVC

Proyecto construido con Maven

Lectura y escritura de archivos con CsvUtil

Interfaz por consola (ConsoleView)

Código modular y mantenible

Los datos permanecen guardados incluso al cerrar el programa o apagar la computadora

Estructura del proyecto:
contenido-audiovisual/
src/
main/
java/
edu.app.contenido
edu.app.contenido.controller
edu.app.contenido.model
edu.app.contenido.repo
edu.app.contenido.service
edu.app.contenido.view
resources/
data/peliculas.csv
test/
java/
pom.xml
README.txt

Arquitectura MVC:

Modelo:
Contiene las clases que representan los datos del sistema, como Pelicula y ContenidoAudiovisual.

Vista:
Contiene ConsoleView, que se encarga de mostrar el menú y leer los datos del usuario desde la consola.

Controlador:
Contiene AppController, encargado de coordinar la comunicación entre la vista, el servicio y el repositorio.

Servicio:
Contiene CatalogoService, donde se aplican las reglas de negocio como listar y agregar películas.

Repositorio:
Contiene ContenidoCsvRepository y CsvUtil, responsables de leer y escribir datos en el archivo CSV.

Persistencia de datos:
El archivo de almacenamiento se encuentra en:
src/main/resources/data/peliculas.csv

Ejemplo de contenido:
P1,Inception,2010,148
P2,Interstellar,2014,169
P3,Matrix,1999,136

Cómo ejecutar el proyecto:

Requisitos:
Java 17 o superior
Maven 3.8 o superior

Compilar el proyecto:
mvn clean install

Ejecutar el programa desde Eclipse:
Clic derecho sobre Main.java
Run As → Java Application

Menú del programa:
=== Contenido Audiovisual ===

Listar películas

Agregar película

Salir

Para agregar una película, el programa solicita:

ID

Título

Año

Duración en minutos

El registro se guarda automáticamente en el archivo peliculas.csv.

Pruebas unitarias:
El proyecto incluye dependencias de JUnit 5 dentro del archivo pom.xml.
Para ejecutar pruebas:
mvn test

Tecnologías utilizadas:
Java 17
Maven
JUnit 5
Patrón MVC
POO
Archivo CSV como almacenamiento

Autor:
Proyecto desarrollado como práctica de POO, persistencia y arquitectura MVC en Java.
