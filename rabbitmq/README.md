# RabbitMq en Docker
RabbitMQ es un software de agente de mensajes de código abierto. Acepta mensajes de productores y los entrega a los consumidores.
### Info
- Wiki: https://es.wikipedia.org/wiki/RabbitMQ
- Site: https://www.rabbitmq.com/

### Instalación
### Docker
- Descargar la imagen con el siguiente comando
    ```sh
    docker pull rabbitmq:3.8-management-alpine
    ```
- Iniciar la limagen
    ```sh 
    docker run -p 15672:15672 -p 5672:5672 --name microservicios-rabbitmq38 --network springcloud -d rabbitmq:3.8-management-alpine
    ```
- Ver los logs del contenedor
    ```sh
    docker logs -f microservicios-rabbitmq38
    ```
### Web Manager
- Una vez iniciado el contenedor abir el navegador y escribir localhost:15672
- El usuario por defecto es: guest
- La contraseña por defecto es: guest