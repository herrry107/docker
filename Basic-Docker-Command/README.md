To see all images present in your local machine
<pre><code>docker images</code></pre>
<pre><code>docker image ls</code></pre>

To find image in docker hub
<pre><code>
#docker search name
docker search ubuntu
</code></pre>

To download image from dockerhu to local machine
<pre><code>docker pull jenkins</code></pre>

To run container with specific name and interactive mode
<pre><code>
docker run -it --name pratik ubuntu /bin/bash
# run: create and start
# -it: interactive mode
# --name: container name
</code></pre>

To run docker container in background
<pre><code>
docker run -d --rm ubuntu /bin/bash
# run: create and start
# -d: background
# --rm: auto remove
</code></pre>

docker port binding with machine port
<pre><code>
docker run -p 5000:3000 image-name
# -p: define port number first one is host machine port and seconde one is container port
</code></pre>

Check port is expose or not
<pre><code>docker port container-name</code></pre>

To check docker service is start or not
<pre><code>
service docker status
service docker start
docker info
</code></pre>

To go inside container
<pre><code>
docker attach container-name
</code></pre>

Similar like attach command but create new process
<pre><code>docker exec -it con1 /bin/bash</code></pre>

To see all containers
<pre><code>
docker ps -a
</code></pre>

To see running containers
<pre><code>
docker ps
</code></pre>

Start and Stop Container
<pre><code>
docker start container-name
docker stop container-name
</code></pre>

Exit from container withou stopping container
<pre><code>
Ctrl + P  then  Ctrl + Q
</code></pre>

Delete container
<pre><code>
docker rm container-name
docker remove container-name  #both command are same
</code></pre>

Create image from container
<pre><code>
#create one container first
docker run -it --name ubuntu1 ubuntu /bin/bash

# command run inside container
cd tmp/
echo "$(hostname)" > test.txt

#Now exit from container
#Now if you want to see the difference between the base image and changes in container
docker diff ubuntu1

#Now create image of this container
#docker commit container-name new-image-name
docker commit ubunut1 updated-image
</code></pre>

if we want to ignore some file when build docker image file name .dockerfile
.dockerfile
<pre><code>
Dockerfile
.git
</code></pre>


