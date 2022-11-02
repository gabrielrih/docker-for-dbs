# Testing
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