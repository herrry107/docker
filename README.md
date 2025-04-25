**Docker is a platform that allows developers to package applications and their dependencies into containers. These containers are lightweight, portable, and consistent across different environments—making it easier to develop, ship, and run software anywhere.**


![Alt-text](https://github.com/herrry107/docker/blob/main/images/docker-architecture.jpg)

**Container:** A way to package an application with all the necessary dependencies and configuration
- It can be easily shared
- Makes Deployment & Development Efficient

**Docker Theory:** 
- Docker is an Open Source centralised platform designed to create, deploy & run applications
- Docker uses container on the host OS to run application. It allows applications to use the same linux Kernel as a system on the host computer, rather than creating a whole virtual OS.
- We can install docker on any OS but Docker engine run natively on linux distribution.
- Docker Written in **GO** language.
- Docker is a tool that perform OS level virtualization, also known as containerization.
- Before Docker many users faces the problem that a particular code is running in the developer system but not in the users system.
- Docker was first release in March 2013 it is developed y solomon nykes and sebastian panl.
- Docker is a set of platform as a service that uses OS level virtualization whereas VMware uses hardware level virtualization.

**Difference between Docker Container vs VMs**

**Docker Container:** 
- Low impact on OS, very fast, low disk space usage.
- Sharing, distribution and re-building is easy.
- Encapsulate apps instead of whole machine.

**VMs:** 
- High impact on OS, Slower, high disk usage.
- Sharing, rebuilding and distribution is challenging.
- Encapsulate whole machine. 
