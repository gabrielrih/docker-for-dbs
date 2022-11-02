# docker-for-dbs
Helpful docker for Databases. It can be used for testing and learning purpose. You can use this by **Docker Compose** or using a **Dockerfile**.

## Installation
Installing docker and docker-compose. Reference: https://docs.docker.com/engine/install

### Installing on Ubuntu
First of all set up the repository and then install these packages:
```
sudo apt update
sudo apt install docker.io
sudo apt install docker-compose
```

## 1. Using Docker Compose
This method will use the **docker-compose.yml** file to create the container.

### Putting UP a container
```
cd postgresql
docker-compose up -d
```

### Putting DOWN a container
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

### Putting UP a container
```
docker run -d --name my-pg-db-container-name -p 5432:5432 my-pg-db-image-name
```

### Putting DOWN a container
```
docker stop <containerId>
docker rm <containerId>
```

## Usefull commands
Showing all container:
```
docker ps
```
Images list:
```
docker images -a
```
Connecting into a running container:
```
docker exec -it <containerId> bash
```

## How to make it works on WSL
- On Windows, you must install Docker Desktop, Rancher Desktop or other similar software.
- Then you need to expose the kubernetes configurations and docker socket on WSL in the software "Preferences".