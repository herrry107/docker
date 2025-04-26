![Alt-text](https://github.com/herrry107/docker/blob/main/images/docker-image-container.png)
![Alt-text](https://github.com/herrry107/docker/blob/main/images/components-of-docker.jpg)

**1. Docker Daemon:** 
- Docker daemon runs on the HOST OS.
- It is responsible for running containers to manage docker service.
- Docker Daemon can communicate with other daemons.

**2. Docker Client:**
- Docker user can interact with docker through a client.
- Docker client uses commands and Rest API to communicate with the docker daemon.
- When a client runs any server command on the docker terminal, the client terminal sends these docker commands to the docker daemons.
- It is possible for docker client to communicate with more than one daemon.

**3. Docker Host:**
- Docker Host is used to provide an environment to execute and run application. It container the docker daemon, images, containers network and storages.

**4. Docker Hub/Registry:**
Docker registory mangaes & Stores the docker images
- Therer are 2 types of registery: 
- **1) Public Registry:** Public registery is also called as docker hub.
- **2) Private Registry:** It is used to share image within the enterprise

**5. Docker Images:**
- Docker images are the read only binary templates used to create docker containers or single file within the all dependencies and configuration required to run a program.

***ways to create images***
1) Take image from docker hub.
2) Create image from docker file.
3) Create image from existing docker container.

**6. Docker Container:**
- Containers hold the entire packages that is needed to run the application, In other words, we can say that, the image is a template and the container is a copy of that template.
- Container is like a virtual machine.
- Images becomes container when they run on docker engine.  
