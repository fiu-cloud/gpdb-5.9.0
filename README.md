# gpdb-5.9.0-docker
Pivotal Greenplum Database Base Docker Image 5.9.0
Ubuntu 16.04

Uses https://github.com/greenplum-db/debian-release and 
loosely based on 
https://github.com/dbbaskette/gpdb-docker 

Note: gpinitsystem is run on the first time the container is run *(not in the docker build)*. This will facilitate future multi-node deployments [TODO] 

# Running the Docker Image
```
docker run -i -t -p 5432:5432 -d fiucloud/gpdb-5.9.0
```

*The first time the container is run it will take a few minutes to initialise the database*

# Container Accounts
root/pivotal

gpadmin/pivotal

# Using psql in the Container
su - gpadmin
psql

# Using pgadmin outside the Container
Launch pgAdmin4
```
username: gpadmin
default db: gpadmin
password: pivotal
port: 5432
```

