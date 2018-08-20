### ewsdocker/alpine-nginx:0.0.3
An un-modified NGINX HHTP Web server image in an Alpine Linux container. 
____  

**Visit the [ewsdocker/alpine-nginx](https://github.com/ewsdocker/alpine-nginx/wiki) Wiki for complete documentation.**  
____  

The **ewsdocker/alpine-nginx** docker image is based on the latest _NGINX_ mainline version (_edge_) in an  _Alpine Linux_ **edge** docker image.  

- A pre-built **ewsdocker/alpine-nginx Docker** image is available on [Docker Hub](https://hub.docker.com) at [ewsdocker/alpine-nginx](https://hub.docker.com/r/ewsdocker/alpine-nginx/);

- The source for **ewsdocker/alpine-nginx** is available on [GitHub](https://github.com/) at [ewsdocker/alpine-nginx](https://github.com/ewsdocker/alpine-nginx).  

____  

The **ewsdocker/alpine-nginx** docker image is **NOT** an official release of **NGINX**.  
  
- The **official release** of **NGINX** is available on [GitHub](https://github.com/) from [NGINX, Inc.](https://github.com/nginxinc);  
  
- The **official build** of **NGINX** is available on [Docker Hub](https://hub.docker.com) at [NGINX, Inc.](https://hub.docker.com/_/nginx/).  

____  

**Visit the [ewsdocker/alpine-nginx](https://github.com/ewsdocker/alpine-nginx/wiki) Wiki for complete documentation.**  
____  

#### Installing ewsdocker/alpine-nginx  

Below are presented two examples of the many ways to download, create and start the service container.  Both examples have strengths and weaknesses.  

1. **Docker Volume**  
   This is the easiest procedure to understand.  It uses the _volume_ option to map the _NGINX_ html folder in the **alpine-nginx** container to a **Docker host** folder (in the calling user's home folder) to be used for the _NGINX_ html folder.  
2. **Docker Mount**  
   This procedure uses the _mount_ option of the _docker run_ command to map a **Docker Volume** on the **Docker Host** to the **alpine-nginx** _NGINX_ html folder.  It requires creation of a **Docker Volume**, which adds to the complexity. However, the benefit is that it is a **Docker** volume and not a _user's_ folder;

In both approaches, the image will be 
- downloaded (if not already present), 
- built into a web service container (if not already present), and 
- started on **port 80**.  

____  

**Docker Volume.**
  
In this example, the **.local/shared/nginx-html** folder (in the calling user's home directory) will contain the html documents to serve.  HTML data (Web Pages) to be served should be added to the _nginx-html_ folder.  

Execute the following _docker run_ command to download the image, create a service container and start the service on port 80:

    docker run -d \
               --restart unless-stopped \
               -v ${HOME}/.local/shared/nginx-html:/usr/share/nginx/html \
               -p 80:80 \
               --name=alpine-nginx-0.0.3 \
           ewsdocker/alpine-nginx:0.0.3  
____  
  
**Docker Mount.**
  
This procedure uses the _mount_ option to mount a **Docker** volume to be used for the _NGINX_ html folder.  

 + Check for existence of the **nginx-html** volume:  
    
    docker volume inspect nginx-html
    
 + If the response is **Error: No such volume: nginx-html**, create the volume:

    docker volume create nginx-html  

HTML data (Web Pages) to be served should be added to the _nginx-html_ volume, starting in the /, or root, directory.  

Execute the following _docker run_ command to download the image, create a service container and start the service on port 80:

    docker run -d \
               --restart unless-stopped \
               --mount source=nginx-html,target=/usr/share/nginx/html \
               -p 80:80 \
               --name=alpine-nginx-0.0.3 \
           ewsdocker/alpine-nginx:0.0.3  
____  
  
**Visit the [ewsdocker/alpine-nginx](https://github.com/ewsdocker/alpine-nginx/wiki) Wiki for complete documentation.**  
____  

**Copyright © 2018. EarthWalk Software.**  
**Licensed under the GNU General Public License, GPL-3.0-or-later.**  

This file is part of **ewsdocker/alpine-nginx**.  

**ewsdocker/alpine-nginx** is free software: you can redistribute 
it and/or modify it under the terms of the GNU General Public License 
as published by the Free Software Foundation, either version 3 of the 
License, or (at your option) any later version.  

**ewsdocker/alpine-nginx** is distributed in the hope that it will 
be useful, but WITHOUT ANY WARRANTY; without even the implied warranty 
of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.  

You should have received a copy of the GNU General Public License
along with **ewsdocker/alpine-nginx**.  If not, see 
<http://www.gnu.org/licenses/>.  
