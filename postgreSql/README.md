# PostgreSql en Docker

### Info 
- Wiki: https://es.wikipedia.org/wiki/PostgreSQL
- Site: https://www.postgresql.org/

### Instalación 
### Docker 
- Descargar la imagen en docker
    ```sh
    docker pull postgres:lastest
    ```
- Iniciar el contenedor    
    ```sh
    docker run -p 5432:5432 --name microservicios-postgres --network springcloud -e POSTGRES_PASSWORD=sasa -e POSTGRES_DB=db_springboot_cloud -d postgres
    ```
- Ver los logs del contenedor 
    ```sh
    docker logs -f microservicios-postgres
    ```
### Docker Compose 
- Posicionarse en la misma ruta que el archivo docker-compose.yml y ejecutar el siguiente comando
    ```sh
        docker-compose up
    ```
### PostgreSql Manager
- Abrir el navegador y escribir la siguiente ruta http://localhost:16543/browser/
- El usuario y contraseña son los que están definidos en el archivo docker-compose.yml 


### Referencias
- https://medium.com/@renato.groffe/postgresql-pgadmin-4-docker-compose-montando-rapidamente-um-ambiente-para-uso-55a2ab230b89