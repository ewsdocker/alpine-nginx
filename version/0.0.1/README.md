# EarthWalkSoftware/alpine-nginx  

The **earthwalksoftware/alpine-nginx** docker image is based on the latest _NGINX_ mainline version (_edge_) in an  _Alpine Linux_ edge docker image.  

The **earthwalksoftware/alpine-nginx** pre-built Docker image is available from [earthwalksoftware/alpine-nginx](https://hub.docker.com/r/earthwalksoftware/alpine-nginx/) at the EarthWalk Software presence on Docker Hub.

----

#### Not A Stable Branch ####
 
This release is **NOT** based upon the _stable_ branch of **NGINX**.  It is based on the very latest, **unstable** (a.k.a. _Bleeding Edge_) releases of both **NGINX** and **Alpine Linux**.

----  

#### Not Official Release / Build  ####  

The **earthwalksoftware/alpine-nginx** docker image is **NOT** an official release of **NGINX**.  
  
- The **official release** of **NGINX** is available from [NGINX, Inc.](https://github.com/nginxinc) at  https://github.com/nginxinc/docker-nginx  
  
- The **official build** of **NGINX** is available from [NGINX, Inc.](https://github.com/nginxinc) at the following location  https://hub.docker.com/_/nginx/  

----

#### The Bleeding Edge ####  

The **earthwalksoftware/alpine-nginx** is **very** experimental.  It is based upon the latest **NGINX** mainline version docker source in the latest (edge)  __Alpine Linux__ docker image.  

This repository contains only the latest **mainline version of Alpine Linux NGINX** code.

Why?  **NGINX** in **Alpine Linux** is a very small image, under 18 MB, yet is powerful enough to easily serve static web sites.  

It's fun finding new uses for this little server.  Check out this twisted use: [pkgcache - a simple "plug in" for Docker build](https://github.com/EarthWalkSoftware/alpine-nginx/wiki/pkgcache----a-simple-%22plug-in%22-for-Docker-build)  

----  

#### Running NGINX ####  

Official documentation for the **NGINX** image is available from [NGINX, Inc. on Docker Hub](https://hub.docker.com/_/nginx/).  

**Note**: When using the instructions, replace the container name **nginx** with **earthwalksoftware/alpine-nginx**

------
### The name's too long
So, give it a shorter name, such as **alpine-nginx**.

Pull the image down to the local docker host:  

    docker pull earthwalksoftware/alpine-nginx:latest  

Tag the new image with a shorter name (e.g. - **alpine-nginx:latest**):  

    docker tag earthwalksoftware/alpine-nginx:latest alpine-nginx:latest  

Remove the original image tag:  

    docker rmi earthwalksoftware/alpine-nginx:latest  

View docker images  

    docker images  

The **alpine-nginx:latest** image is now located on the local docker host.  The image may be accessed as **alpine-nginx**

----  

#### A unique use for the alpine-nginx server  

To see a unique use of the **alpine-nginx** server, visit this article on the _EarthWalk Softare alpine-nginx wiki_: [pkgcache - a simple "plug in" for Docker build](https://github.com/EarthWalkSoftware/alpine-nginx/wiki/pkgcache----a-simple-%22plug-in%22-for-Docker-build)

----  

#### License ####  

The **EarthWalkSoftware/alpine-nginx** is controlled by the **NGINX License**, available at https://hub.docker.com/_/nginx/  

A copy of the License is available inside the running container as a text file in the root directory: **/LICENSE**. and in the docker source on GitHub: https://github.com/EarthWalkSoftware/alpine-nginx

----  
