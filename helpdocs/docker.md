# list all docker logins (look in auths)
cat ~/.docker/config.json

# login dockerhub 
docker login 

# show local images - grep this as needed 
docker images 

# remove an image 
docker rmi darylhandleysonatype/test-private-image:latest

# pull an image from dockerhub 
docker pull darylhandleysonatype/test-private-image:latest

# pull an image from my local using path based support 
# (must allow insecure registries first)
docker pull darylhandleysonatype/test-private-image:latest

# execute a command on your container 
docker exec -it nexus cat /nexus-data/admin.password

# shell into your container 
docker exec -it nexus bash

# ---------------------------------------------------------
# allow insecure registries for a docker repo 
# ---------------------------------------------------------
vi /etc/docker/daemon.json

# add a line like this 
{
  "insecure-registries": ["localhost:5555"]
}

# restart docker from docker desktop 

# ---------------------------------------------------------
