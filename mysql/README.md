#  Mysql en Docker

### Info
- Wiki : https://es.wikipedia.org/wiki/MySQL
- Site: https://www.mysql.com/

### Instalación
### Docker
- Descargar la imagen en docker
    ```sh
    docker pull mysql:8
    ```
- Iniciar el contenedor    
    ```sh
    docker run -p 3306:3306 --name microservicios-mysql8 --network springcloud -e MYSQL_ROOT_PASSWORD=sasa -e MYSQL_DATABASE=db_springboot_cloud -d mysql:8
    ```
- Ver los logs del contenedor 
    ```sh
docker logs -f microservicios-mysql8
    ```

### Conexión por consola de Docker
- Ejeuctar la siguiente instrucción para conectarse al servidor de mysql
    ```sh
    docker exec -it microservicios-mysql8 mysql -uroot -p
    ```
### Nota
- El servicio de mysql demora un poco por lo se debe verificar en los logs si el contenedor esta listo caso contrario no se podrá conectar con un manager como WorkBench