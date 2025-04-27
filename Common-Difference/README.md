**Difference between docker attach and docker exec**
- Docker exec creates a new process in the containers environment while docker attach just connect the standard input/output of the main process inside the container to corresponding standard input/output error of current terminal.
- docker exec is specifically for running new thing in a already started container, be it a shell or some other process.

**Difference between expose and publish a docker**
Basically we have 3 options:
1) Neither specify **expose** not **-p**: the service in the container will only be accessible from inside the container itself.

2) Only specify **expose**: If you expose a port, the service in the container is not accessible from outside docker, but from inside other docker container, so this is good for inter-container communication.

3) Specify **expose** and **-p**: access from outside and inside.
  
