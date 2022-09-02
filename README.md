# docker-for-dbs
Docker compose for Databases. It can be used for testing and learning purpose. 

## Installation
Installing docker and docker-compose. Reference: https://docs.docker.com/engine/install

### Installing on Ubuntu
First of all set up the repository and then install these packages:
```
sudo apt update
sudo apt install docker.io
sudo apt install docker-compose
```

## How to use it
### Putting UP a container
Example using postgreSQL:
```
cd postgresql
docker-compose up
```

### Putting DOWN a container
```
docker-compose down
```

## How to make it works on WSL
PUT THE TEXT HERE
- Install on Windows Docker Desktop, Rancher Desktop or other similar software.
- Then, do this on WSL: https://nickjanetakis.com/blog/setting-up-docker-for-windows-and-wsl-to-work-flawlessly#configure-docker-for-windows
```
echo "export DOCKER_HOST=tcp://localhost:2375" >> ~/.bashrc && source ~/.bashrc
```