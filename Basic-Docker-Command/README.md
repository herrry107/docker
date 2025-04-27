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

To run container with specific name
<pre><code>
docker run -it --name pratik ubuntu /bin/bash
# run: create and start
# -it: interactive mode
# --name: container name
</code></pre>


