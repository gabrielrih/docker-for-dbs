## Using Dockerfile

### Creating the image on your local repository
```
cd rabbitmq
docker build -t my-rabbit .
```
Review if the image was created:
```
docker images -a
```

### Putting UP the container
```
docker run -d --name my-rabbit -p 5672:5672 -p 15672:15672 my-rabbit
```

### Putting DOWN the container
```
docker stop <containerId>
docker rm <containerId>
```

### Exposed ports
- 5672: Rabbit main service
- 15672: Management plugin/Web Site (http://localhost:15672/#/)

### References:
- https://hub.docker.com/_/rabbitmq
