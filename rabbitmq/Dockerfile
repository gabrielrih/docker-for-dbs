# References:
#   https://hub.docker.com/_/postgres
#   https://dev.to/andre347/how-to-easily-create-a-postgres-database-in-docker-4moj
FROM rabbitmq:3-management
ENV RABBITMQ_DEFAULT_USER rabbitmq
ENV RABBITMQ_DEFAULT_PASS password
ENV RABBITMQ_NODE_PORT 5672

# Rabbit main service and Management plugin ports
EXPOSE 5672
EXPOSE 15672