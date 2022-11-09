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
See the exposed ports to a container:
```
docker port <containerName>
```

## How to make it works on WSL
- On Windows, you must install Docker Desktop, Rancher Desktop or other similar software.
- Then you need to expose the kubernetes configurations and docker socket on WSL in the software "Preferences".

## Some reference:
- Expose ports: https://www.baeldung.com/ops/docker-expose-more-than-one-portddd