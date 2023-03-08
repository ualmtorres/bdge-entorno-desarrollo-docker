# Configuración del entorno de la asignatura con Docker


El archivo `docker-compose.yml` contiene los servicios necesarios para desplegar y poder practicar con las principales bases de datos usadas en la asignatura de Bases de datos a gran escala. Está formado por servicios para Redis, MongoDB y Neo4j.

* Iniciar con `docker-compose up - d`
* Detener con `docker-compose down`

## Servicios disponibles

* Redis: puerto 6379
* MongoDB: puerto 27017
* Neo4j: puerto 7687

También se despliegan interfaces web para su administración. Son las siguientes:

* RedisInsight: puerto 8001
* Mongo Express: puerto 8081
* Neo4j: puerto 7474

## Variables de entorno

Las variables de entorno (básicamente usuarios y contraseñas) se configuran en el archivo `.env`.

## Persistencia

Los datos las bases de datos Redis, MongoDB y Neo4j se almacenan en _bind mounts_ como subcarpetas de la carpeta donde está `docker-compose.yml`.

* `./mongo-data` almacena los datos de MongoDB
* `./neo4j-data` almacena los datos de Neo4j
* `./redis-data` almacena los datos de Redis