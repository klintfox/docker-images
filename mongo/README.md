#  MongoDB en Docker

### Info 
- Wiki: https://es.wikipedia.org/wiki/MongoDB
- Site: https://www.mongodb.com/cloud/atlas

### Instalación 
### Docker 
- Descargar la imagen en docker
    ```sh
    docker pull mongo:latest
    ```
Iniciar el contenedor    
    ```sh
    docker run -p 27001:27001 --name mongo --network mongonet -d mongo:latest
    ```
- Ver los logs del contenedor 
    ```sh
    docker logs -f mongo
    ```
### Docker Compose 
- Posicionarse en la misma ruta que el archivo docker-compose.yml y ejecutar el siguiente comando
    ````sh
        docker-compose up
    ```