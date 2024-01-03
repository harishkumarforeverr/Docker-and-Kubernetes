# links

https://hub.docker.com/_/node

# commands

1. copying file from local system to container
   COPY ./(from ur local system, path must be relative to build context) ./(to vitual machine, Container)

2. PORT
   docker run -p 8080:8080 <imageId>
   here LHS 8080 is coming from the localshot which we calll in browser url
   here RHS 8080 is the port no inside the conatiner which we write app.js file
   example : docker run -p 8080:8080 harish/simpleserver

3. OPEN SHELL
   docker run -it harish/simpleserver sh (here sh is main command to open the termainal)

4. working direct setup manaully
  WORKDIR /usr/app

5. excute the container in 2nd terminal
   docker ps
   docker exec -it <containerId> sh