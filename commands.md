- docker start `<image name>` or same above command can be user in aother

  docker create `<image name>`
  << id
  docker start id // outpuut we will get commlpeted id of conatiner
  docker start -a id // it will show all the images
  or
  same above command can be use in another way like docker logs id

- docker ps // will list all the active runnning docker container

- docker ps --all // list all the docker till now we run

- doker system prune /// command will remove all the history of container from cmd which we runned in previous

- to stop the container
  docker stop containerId

- to kill the container
  docker kill containerId

- docker exec -it containerId extra-command
  eg: docker exec -it containerId redis-cli // here -it means stdin and stdoout

  PS C:\Users\Dev2Prod> docker exec -it c836f18f5741 redis-cli
  127.0.0.1:6379> set myvalue 5
  OK
  127.0.0.1:6379> get myvalue
  "5"
  127.0.0.1:6379>

- docker exec -it c836f18f5741 sh // sh command is used to perform the schell commands like same as the command prompt

- to see the folder stuture
  PS C:\Users\Dev2Prod> docker exec -it c836f18f5741 sh
  ls
  cd ~/
  ls
  cd /
  ls
  bin boot data dev etc home lib lib32 lib64 libx32 media mnt opt proc root run sbin srv sys tmp usr var

- example of sh command
  PS C:\Users\Dev2Prod> docker run -it busybox sh
  / # echo hi
  hi
  / # ls
  bin dev etc home lib lib64 proc root sys tmp usr var
  / # ping google.com
  PING google.com (142.250.182.206): 56 data bytes
