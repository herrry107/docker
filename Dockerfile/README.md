Dokcerfile is basically a text file. It contains some set of instruction. Automation of Docker image creation.
**Docker Components**
- ***FROM:*** for base image this command must be on top of the Dockerfile.

- ***RUN:*** To execute commands, it will create a layer in image.

- ***MAINTAINER:*** Author/Owner/Description.

- ***COPY:*** Copy files from local system to (Docker VM), We need to provide source, destination (We can't download file from internet and any remote repo).

- ***ADD:*** Similar to copy but it provides a features to download files from internet also we extract file at docker image side.

- ***EXPOSE:*** To expose ports such as port 8080 for tomcat, port 80 for nginx etc.

- ***CMD:*** Execute commands but during container creation.

- ***ENTRYPOINT:*** Similar to CMD but has higher priority over CMD, first commands will be executed by ENTRYPOINT ony.

- ***ENV:*** Environment Variables.
