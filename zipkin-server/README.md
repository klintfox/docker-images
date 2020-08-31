#  Zipkin
Zipkin es un sistema de rastreo distribuido. Ayuda a recopilar los datos de tiempo necesarios para solucionar problemas de latencia en arquitecturas de servicio. Las características incluyen tanto la recopilación como la búsqueda de estos datos.
### Info
- Wiki: 
- Site: https://zipkin.io/
### Docker
-  En windows abrir la consola de comandos
- Para descargar la imagen de dockerHub ejecutar el siguiente comando
    ```sh
    docker pull openzipkin/zipkin
    ```
- Para levantar un contenedor ejecutar la siguiente instrucción:
    ```sh
    docker run -d -p 9411:9411 openzipkin/zipkin
    ```
### Zipkin con RabbitMq y Mysql
- Crear un contenedor mysql y configurar un usuario crear un usuario zipkin (ver proyecto mysql)
- Crear el schema en mysql para el usuario zipkin
- Crear un contenedor de rabbitMq (ver proyecto rabbitmq)
- Ejecutar la siguiente instrucción para ejecutar un contenedor de zipkin
    ```sh
    docker run -d -p 9411:9411 openzipkin/zipkin --network springcloud -e RABBIT_ADDRESSES=microservicios-rabbitmq38:5672 -e STORAGE_TYPE=mysql -e MYSQL_USER=zipkin -e MYSQL_PASS=zipkin -e MYSQL_HOST=microservicios-mysql8 openzipkin/zipkin:lastest
    ```
- Para ver los logs del contenedor ejecutar el siguiente comando
    ```sh
    docker logs -f openzipkin/zipkin
    ```