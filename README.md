Docker basic commands

1.Check ?
How are we setting up commandline to authenticate

2.Once authenticated build Dockerfile
 docker build --tag="Name"

3.docker image ls
Lists the images built

4.docker container ls
Lists the containers running

5.docker run -p 4000:80 "TAG NAME"
Should run the app.

More about Docker image :

> An image is never running The docker run command takes the Docker image as a template and produces a container from it.

Docker build:
-------------
Docker build helps create an image. The command is 
 docker build -t repo:tag .
The . indicates context. The image bundles everything that is in the current folder as part of the image and it reflects in the size of the image.
In order to exclude any files being copied into the image, we need to use a dockerignore file.
We can inspect an image using the command
docker image inspect (identifier)
docker run -ti "image tag" bash , opens up the contents of the image

Docker container
----------------

Docker container is built from an image and it has an extra writable layer on top of the image. As each container has its own writable container layer, and all changes are stored in this container layer, multiple containers can share access to the same underlying image and yet have their own data state.


