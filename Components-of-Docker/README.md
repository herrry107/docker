![Alt-text](https://github.com/herrry107/docker/blob/main/images/docker-image-container.png)
![Alt-text](https://github.com/herrry107/docker/blob/main/images/components-of-docker.jpg)

**Docker Daemon: ** 
- Docker daemon runs on the HOST OS.
- It is responsible for running containers to manage docker service.
- Docker Daemon can communicate with other daemons.

**Docker Client: **
- Docker user can interact with docker through a client.
- Docker client uses commands and Rest API to communicate with the docker daemon.
- When a client runs any server command on the docker terminal, the client terminal sends these docker commands to the docker daemons.
- It is possible for docker client to communicate with more than one daemon.

**Docker Host: **
- Docker Host is used to provide an environment to execute and run application. It container the docker daemon, images, containers network and storages.

**Docker Hub/Registry: **
Docker registory mangaes & Stores the docker images
- Therer are 2 types of registery: 
- **1) Public Registry: ** Public registery is also called as docker hub.
- **2) Private Registry: ** It is used to share image within the enterprise 
