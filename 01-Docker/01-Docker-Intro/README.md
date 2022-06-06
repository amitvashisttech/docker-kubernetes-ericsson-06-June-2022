```    
   14  cd 00-Vagrant-Setup/
   15  ls
   16  vim README.md 
   17  ls
   18  cd ..
   19  ls
   20  vim /root/.bashrc 
   21  source /root/.bashrc
   22  ls
   23  git add . ; git commit -m "00-Vagrant-Setup" ; git push 
   24  ls
   25  mkidr 01-Docker
   26  mkdir 01-Docker
   27  cd 01-Docker/
   28  ls
   29  cp -rf /root/old/01-Docker/00-Setup . 
   30  ls
   31  mkdir 01-Docker-Intro
   32  ls
   33  cd 00-Setup/
   34  ls
   35  ./install-docker.sh 
   36  docker version 
   37  ls
   38  cd ..
   39  ls
   40  docker images 
   41  docker container ls 
   42  docker container ls -a 
   43  docker run busybox echo "Hello World" 
   44  docker container ls 
   45  docker container ls -a
   46  docker run busybox echo "Hello World" 
   47  docker run busybox echo "Welcome to the world of docker." 
   48  docker images 
   49  docker run ubuntu echo "Welcome to the world of docker." 
   50  docker ps 
   51  docker ps -a 
   52  cat /etc/os-release 
   53  docker run ubuntu  cat /etc/os-release
   54  docker images 
   55  docker ps -a 
   56  cat /etc/os-release 
   57  docker run ubuntu:16.04  cat /etc/os-release
   58  docker images 
   59  docker search ubuntu 
   60  docker search ubuntu --help
   61  docker search ubuntu:16.04
   62  curl -L -s 'https://registry.hub.docker.com/v2/repositories/library/mysql/tags/' | jq . | grep name
   63  apt-get install jq
   64  curl -L -s 'https://registry.hub.docker.com/v2/repositories/library/mysql/tags/' | jq . | grep name
   65  curl -L -s 'https://registry.hub.docker.com/v2/repositories/library/ubuntu/tags/' | jq . | grep name
   66  docker ps 
   67  docker ps -a
   68  docker run ubuntu:16.04 --name test-1  cat /etc/os-release
   69  docker run --name test-1 ubuntu  cat /etc/os-release
   70  docker ps -a 
   71  docker rename 8bae2f9e6b7b test-5 
   72  docker ps -a 
   73  ls
   74  cd 01-Docker-Intro/
   75  ls
   76  history > README.md
```
