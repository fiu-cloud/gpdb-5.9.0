# gpdb-5.9.0-docker
Pivotal Greenplum Database Base Docker Image 5.9.0
Ubuntu 16.04

https://github.com/greenplum-db/debian-release and 
loosely based on https://github.com/dbbaskette/gpdb-docker. 

Note: gpinitsystem is performed the first time the container is run (not in the build). This will enable future multi-node deployments [TODO] 


cd [docker working directory]

docker build -t [tag] .

# Running the Docker Image
docker run -i -t -p 5432:5432 -d [tag]
# Container Accounts
root/pivotal

gpadmin/pivotal

# Using psql in the Container
su - gpadmin

psql

# Using pgadmin outside the Container
Launch pgAdmin3

Create new connection using IP Address and Port # (5432)
