
# Starting the container

## 1. Using Docker Compose
This method will use the **docker-compose.yml** file to create the container.

### Putting UP the container
```
cd postgresql
docker-compose up -d
```

### Putting DOWN the container
```
docker-compose down
```

## 2. Using Dockerfile
This method will use the **Dockerfile** file to create the container.

### Creating the image on your local repository
```
cd postgresql
docker build -t my-pg-db-image-name .
```
Review if the image was created:
```
docker images -a
```

### Putting UP the container
```
docker run -d --name my-pg-db-container-name -p 5432:5432 my-pg-db-image-name
```

### Putting DOWN the container
```
docker stop <containerId>
docker rm <containerId>
```


# Connecting
Once you have the container running, you can test the connect using this command:
```
psql -h localhost -p 5432 -U postgres
```
From connection inside the container you can use just:
```
psql -U postgres
```

# Installing PG client
Change 'X' by the PG number you are using.
```
sudo apt install postgresql-client-X
```