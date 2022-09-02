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
- On Windows, you must install Docker Desktop, Rancher Desktop or other similar software.
- Then you need to expose the kubernetes configurations and docker socket on WSL in the software "Preferences".