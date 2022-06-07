```
323  mkdir 03-DockerVolumes
  324  ls
  325  cd 03-DockerVolumes/
  326  ls
  327  docker volume ls
  328  docker volume create my-vol
  329  docker volume ls
  330  docker volume inspect my-vol
  331  ls -ltr /var/lib/docker/volumes/my-vol/_data
  332  ls -ltr /var/lib/docker/volumes/my-vol/_data/
  333  ls -ltr /var/lib/docker/volumes/
  334  ls
  335  docker run -it --name volume-test-1 -v my-vol:/var/www/html/app ubuntu:16.04
  336  docker ps
  337  cat  /var/lib/docker/volumes/my-vol/_data/Hello.txt
  338  docker ps -a
  339  docker rm $(docker ps -qa)
  340  docker ps -a
  341  docker volumes ls
  342  docker volume ls
  343  cat  /var/lib/docker/volumes/my-vol/_data/Hello.txt
  344  docker run -it --name volume-test-2 -v my-vol:/var/www/html/app ubuntu:16.04
  345  ls
  346  docker ps -a
  347  docker ps
  348  ls
  349*
  350  docker run -it --name volume-test-3 -v /var/www/html/app ubuntu:16.04
  351  docker volume ls
  352  docker volume inspect e0e96160e857337f68f35159b8809b3fb93c3840842e35565b9d0cd0fe81043f
  353  cat /var/lib/docker/volumes/e0e96160e857337f68f35159b8809b3fb93c3840842e35565b9d0cd0fe81043f/_data/hello.txt
  354  history
  355  docker volume ls
  356  docker volume inspect e0e96160e857337f68f35159b8809b3fb93c3840842e35565b9d0cd0fe81043f
  357  cat /var/lib/docker/volumes/e0e96160e857337f68f35159b8809b3fb93c3840842e35565b9d0cd0fe81043f/_data/hello.txt
  358  docker ps
  359  docker volume ls
  360  docker ps
  361  docker inspect volume-test-3
  362  pwd
  363  docker run -it --name volume-test-4 -v /root/docker-kubernetes-ericsson-06-June-2022/01-Docker/03-DockerVolumes:/myapp ubuntu:16.04
  364  ls
  365  cd ..
  366  ls
  367  docker run -it --name volume-test-5 -v /root/docker-kubernetes-ericsson-06-June-2022:/myapp:ro ubuntu:16.04
  368  docker volume ls
  369  docker ps
  370  docker inspect volume-test-5
  371  docker inspect volume-test-4
  372  ls
  373  docker kill  $(docker ps -qa)
  374  docker rm  $(docker ps -qa)
  375  ls
  376  docker volumes ls
  377  docker volume ls
  378  docker volume ls -q
  379  docker volume rm $(docker volume ls -q )
  380  docker volume ls
```
