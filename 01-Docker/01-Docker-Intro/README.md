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

```
 98  docker pull nginx
   99  docker image s
  100  docker images
  101  docker pull amitvashist7/nginx-web
  102  docker pull amitvashist7/nginx-web:v1
  103  docker images
  104  docker pull amitvashist7/nginx-web:v2
  105  docker images
  106  docker inspect amitvashist7/nginx-web:v1
  107  ls
  108  history
  109  docker images
  110  docker delete amitvashist7/nginx-web:v2
  111  docker rmi  amitvashist7/nginx-web:v2
  112  docker images
  113  docker rmi  amitvashist7/nginx-web:v1
  114  docker images
  115  docker pull   amitvashist7/nginx-web:v1
  116  docker pull   amitvashist7/nginx-web:v2
  117  docker images
  118  docker rmi   amitvashist7/nginx-web:v1
  119  docker images
  120  docker inspect amitvashist7/nginx-web:v2
```

```
  134  docker pull amitvashist7/apache-ex4
  135  docker login
  136  docker pull amitvashist7/apache-ex4
  137  docker images
  138  docker logout
  139  docker images
  140  docker pull amitvashist7/apache-ex4:20200107
```

```
  152  docker ps -a
  153  docker run -it ubuntu
  154  docker ps
  155  docker ps -a
  156  docker ps
  157  docker run -it ubuntu
  158  docker ps
  159  docker ps -a
  160  docker ps -a
  161  docker start jolly_mclean
  162  docker ps
  163  docker attach 10e60c254350
  164  docker ps
  165  docker stop jolly_mclean
  166  docker ps
  167  docker ps -a
  168  docker start jolly_mclean
  169  docker ps
  170  docker inspect 10e60c254350
  171  docker ps
  172  docker ps -l
  173  docker ps
  174  docker ps -a
  175  docker ps -q
  176  docker ps
  177  docker ps -qa
  178  docker ps -ql
  179  docker ps -qa
  180  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
  181  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
  182  ls
  183  docker ps
  184  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
  185  docker kill jolly_mclean
  186  docker ps
  187  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
  188  docker stop jolly_mclean
  189  docker start jolly_mclean
  190  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
  191  history
  192  docker ps
  193  docker images
  194  docker run -d --name web-app nginx
  195  docker ps
  196  docker run -itd --name test-n1 ubuntu
  197  docker ps
  198  docker run -d --name test-n2 ubuntu
  199  docker ps
  200  docker ps -a
  201  docker attach test-n1
  202  docker ps
  203  docker attach web-app
  204  docker ps
  205  docker ps -a
  206  docker start 2938e9b5b463
  207  docker ps -a
  208  ls
  209  docker ps
  210  docker ps -a
  211  ls
  212  docker ps -a
  213  docker ps -qa
  214  docker rm $(docker ps -qa )
  215  docker ps
  216  docker ps -a
  217  docker kill $(docker ps -qa )
  218  docker rm $(docker ps -qa )
```
