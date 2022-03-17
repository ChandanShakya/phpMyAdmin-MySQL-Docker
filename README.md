# DOCKER For LAMP Development 

## What this Dockerfile contains?
- Apache
- PHP
- MySQL
- phpMyAdmin

How to run?
- git clone
- cd LAMP-Docker
- Install docker and docker-compose
- To start the container;
```bash
docker-compose up -d
```
> This will spin up a container with apache, MySQL and PHP
> The persisent volume will be named mysql-test
> First run will take longer as it has to fetch all images
- To check if the server is running or not;
    - open localhost:8080
- To list the current running containers;
```bash
docker-compose ps
```
- Put your files in /src folder; it should show up in localhost:8080
- To access phpMyAdmin, navigate to localhost:5000
- To stop the container;
```bash
docker-compose down
```
- To list the volumes
```bash
docker volumes ls
```
- To remove the volume
```bash
docker volume rm phpMyAdmin-MySQL-Docker_sql-test
```
- To remove the images
```bash
# List all the images
docker image ls
# Remove the unneeded images
docker image rm namesOfImages
```

- Default MySQL password = secret
- Default phpMyAdmin user = root
- Default phpMyAdmin password = secret
- Default servername = mysql-server
