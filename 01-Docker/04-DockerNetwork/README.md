```
 450  mkdir 04-DockerNetwork
  451  cd 04-DockerNetwork/
  452  ls
  453  docker ps
  454  docker images
  455  docker run -d --name test-web-server-1 nginx
  456  docker run -d --name test-web-server-2 myapache-img:v2
  457  docker stop test-web-server-1
  458  docker ps
  459  docker inspect test-web-server-2
  460  docker network ls
  461  docker network inspect bf7f2e65bf8a
  462  docker start test-web-server-1
  463  docker network inspect bf7f2e65bf8a
  464  docker inspect test-web-server-2
  465  ip addr
  466  curl 172.17.0.2
  467  curl 172.17.0.3
  468  docker ps
  469  curl 172.17.0.3
  470  curl localhost
  471  netstat -tulnp
  472  docker run -d --name test-web-server-3 -p 80:80 myapache-img:v2
  473  docker ps
  474  netstat -tulnp
  475  systemctl status docker
  476  curl 172.17.0.4:80
  477  curl localhost
  478  curl 172.31.0.100:80
  479  docker run -d --name test-web-server-4 -p 80:80 nginx
  480  docker run -d --name test-web-server-5 -p 81:80 nginx
  481  docker ps
  482  netstat -tulnp
  483  systemctl status docker
  484  docker run -d --name test-web-server-6 -p 81:80 nginx
  485  docker run -d --name test-web-server-7 -P nginx
  486  docker ps
  487  docker run -d --name test-web-server-8 -P myapache-img:v2
  488  docker ps
  489  docker inspect nginx
  490  ls
  491  docker images
  492  docker inspect myapache-img:v2
  493  ls
  494  cd ../
  495  ls
  496  cd 02-DockerImages/
  497  ls
  498  cd apache/
  499  ls
  500  cp -rf v2 v3
  501  ls
  502  cd v3/
  503  ls
  504  vim Dockerfile
  505  ls
  506  docker images
  507  docker build -t myapache-img:v3 .
  508  docker images
  509  docker inspect myapache-img:v3
  510  docker run -d --name test-web-server-9 -P myapache-img:v3
  511  docker ps
  512  ls
  513  cd ..
  514  ls
  515  cp -rf v3 v4
  516  ls
  517  cd v4/
  518  ls
  519  mv Dockerfile apache-exp1
  520  ls
  521  vim index.html
  522  ls
  523  vim apache-exp1
  524  docker build -t myapache-img:v4 .
  525  ls
  526  docker build -t myapache-img:v4 -f apache-exp1 .
  527  docker images
  528  docker inspect myapache-img:v4
  529  docker run -d --name test-web-server-10 -P myapache-img:v4
  530  docker ps
  531  cd
  532  curl telnet://loalhost 32771
  533  curl telnet://loalhost:32771
  534  curl telnet://localhost:32771
  535  curl telnet://localhost 32771
  536  curl -vvv telnet://localhost 32771
  537  curl -vvv telnet://localhost:32771
  538  curl -vvv telnet://localhost:32770
  539  docker ps
  540  docker kill $(docker ps -qa)
  541  ls
  542  docker rm $(docker ps -qa)
  543  ls
  544  docker run -it ubuntu:16.04
  545  docker ps
  546  docker commit -p -m "Net Tools Installed" 4b3d763a9256 ubuntu-nettools:v1
  547  docker images
  548  docker ps
  549  docker run -itd --name test-nw-1 ubuntu-nettools:v1
  550  docker ps
  551  docker exec -it test-nw-1 ifconfig
  552  docker exec -it test-nw-1 ping -c2 google.com
  553  docker exec -it test-nw-1 ping -c2 172.17.0.2
  554  ls
  555  docker network ls
  556  docker network inspect bf7f2e65bf8a
  557  docker network create --help
  558  docker network create --driver "bridge" --subnet=172.28.0.0/16 --ip-range=172.28.5.1/24 --gateway=172.28.5.254 mybr0
  559  docker network ls
  560  docker network inspect mybr0
  561  docker run -itd --name test-nw-2 ubuntu-nettools:v1
  562  docker ps
  563  docker exec -it test-nw-2 ifconfig
  564  docker run -itd --name test-nw-3 --network mybr0 ubuntu-nettools:v1
  565  docker exec -it test-nw-3 ifconfig
  566  docker run -itd --name test-nw-4 --network mybr0 ubuntu-nettools:v1
  567  docker exec -it test-nw-4 ifconfig
  568  docker exec -it test-nw-4 ping -c google.com
  569  docker exec -it test-nw-4 ping -c2 google.com
  570  docker exec -it test-nw-4 ping -c2 172.17.5.0
  571  docker exec -it test-nw-4 ping -c2 172.17.5.1
  572  docker exec -it test-nw-4 ping -c2 172.28.5.1
  573  docker exec -it test-nw-4 ping -c2 172.28.5.0
  574  docker network  ls
  575  docker run -itd --name test-nw-5 --network none ubuntu-nettools:v1
  576  docker exec -it test-nw-5 ifconfig
  577  docker exec -it test-nw-4 ifconfig
  578  docker exec -it test-nw-5 ifconfig
```
