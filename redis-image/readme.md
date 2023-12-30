1. command
   docker build .
   docker run containerId
   <!--  note Dockerfile name should be same letter and in file F msut be small letters -->

2. to give alias name for the conatiner id
   docker build -t yourId/projectName:latest .
   docker run yourId/projectName

3. we will be running a command to create a
   new image using docker commit with this command:

   docker commit -c 'CMD ["redis-server"]' CONTAINERID

   If you are a Windows user you may get an error like "/bin/sh: [redis-server]: not found" or "No Such Container"

   Instead, try running the command like this:

   docker commit -c "CMD 'redis-server'" CONTAINERID
