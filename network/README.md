# network

In Docker, a network allows containers to communicate with each other and with external systems. Docker provides several types of networks for different use cases. Here's an overview:

| Network Type | Description                                                                                                                 |
| ------------ | --------------------------------------------------------------------------------------------------------------------------- |
| **bridge**   | Default for standalone containers. Allows communication between containers on the same host.                                |
| **host**     | Shares the host’s network stack. The container does not get its own IP address.                                             |
| **none**     | No network connectivity. Isolated container.                                                                                |
| **overlay**  | Used in Docker Swarm for multi-host networking. Containers across different Docker daemons can communicate.                 |
| **macvlan**  | Assigns a MAC address to a container, making it appear as a physical device on the network. Useful for advanced networking. |

**List all network**
<pre><code>docker network ls</code></pre>

**inspect network**
<pre><code>docker network inspect network-name</code></pre>

**create network**
<pre><code>
#docker network create network-name
docker network create work
</code></pre>

**create container in defined network**
<pre><code>docker run -it --network work --name con1 ubuntu</code></pre>

**connect to container by network**
<pre><code>
#docker network connect network-name container-name
docker network connect work con2
</code></pre>

