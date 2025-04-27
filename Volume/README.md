**VOLUME**

1) Volume is simply a directory inside our container
2) firstly, we have to declare this directory as a volume and then share volume.
3) Even if we stop container, still we can access volume.
4) Volume will be created in one container.
5) You can declare a directory as a volume only while creating container.
6) You can't create volume from existing container.
7) You can share one volume across any number of containers.
8) Volume will not be included when you update an image.
9) You can mapped volume in two ways
    - Container to Container
    - Host to Container
  
**Benefit Of Volume**
- Decoupling container from storage.
- Share volume among different containers.
- Attach volume to containers.
- On deleting container volume does not delete.

**Creating Volume from Dokcerfile**
<pre><code>
FROM ubuntu
VOLUME ["/myvolume"]
</code></pre>

<pre><code>docker build -t myimage .</code></pre>
Now create a container from this image and run
<pre><code>docker run -it --name con1 myimage /bin/bash</code></pre>
Now you can see folder with name myvolume in container1 which act as a volume

Now share volume with another container
- Container1 to Container2
<pre><code>
#creating container2
docker run -it --name con2 --privileged=true --volumes-from con1 ubuntu /bin/bash
</code></pre>
Now after creating container2, myvolume1 is visible. Whatever you do in one volume, can see from other volume.

create volume by command without Dockerfile
<pre><code>
docker run -it --name con3 -v /volume3 ubuntu /bin/bash
</code></pre>

Now share volume with Host
- Host to Container
<pre><code>
#for linux
docker run -it --name con4 -v /root/docker-practice/vol1:/mycon-vol --privileged=true ubuntu /bin/bash #first path is host path and second one is container path
#for windows
docker run -it --name con4 -v "f:\docker\vol1":/mycon-vol --privileged=true ubuntu /bin/bash    
</code></pre>

