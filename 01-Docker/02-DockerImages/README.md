```
    1  ls
    2  docker ps 
    3  docker ps -a 
    4  docker start test-apache
    5  docker ps 
    6  docker attach test-apache
    7  ls
    8  cd docker-kubernetes-ericsson-06-June-2022/
    9  ls
   10  cd 01-Docker/
   11  ls
   12  mkdir 02-DockerImages/apache/v1 -p 
   13  ls
   14  cd 02-DockerImages/apache/v1/
   15  ls
   16  vim Dockerfile
   17  ls
   18  docker build -t myapache-img:v1 . 
   19  ls
   20  docker images 
   21  docker run -d --name test-apache-v1-1 myapache-img:v1 
   22  docker ps 
   23  docker inspect test-apache-v1-1
   24  curl 172.17.0.3
```
