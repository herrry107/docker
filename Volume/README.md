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
