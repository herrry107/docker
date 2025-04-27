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

**Dockerfile**
1) Create a file named Dockerfile
2) Add instructions in Dockerfile
3) Build Dockerfile to create image
4) Run image to create container

**Dockerfile Example1**
<pre><code>
FROM ubuntu
RUN echo "HEllo World" > /tmp/testfile.txt
</code></pre>

To create image out of Dockerfile
<pre><code>
docker build -t myimg .  #build image from dockerfile
docker ps -a             #show all process
docker images            #show all images
</code></pre>

**Dockerfile Example2**
<pre><code>
FROM ubuntu                            #ubuntu image
WORKDIR /tmp                           #working directoy tmp
RUN echo "Hello World" > testfile.txt  #command run on create image
ENV myname pratik                      #create environment variable with name myname and value pratik
COPY testfile1 /tmp                    #copy from local machine to docker image
ADD test.tar.gz /tmp                   #like copy command
</code></pre>

**Dockerfile Example3**
<pre><code>
FROM node:20            #node image with version 20
WORKDIR /myapp          #working directoy /myapp
COPY . .                #copy all from local that folder to docker image
RUN npm install         #command run on create image
EXPOSE 3000             #expose port number
CMD ["npm","start"]     #run command when container create, cmd command specify by comma
</code></pre>

To build image out of Dockerfile
<pre><code>
docker build -t myimg .  #build image from dockerfile
</code></pre>
