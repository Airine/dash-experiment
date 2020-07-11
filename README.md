# Setup DASH video streaming experiment environment

Steps to setup a DASH client in a Docker Container for downloading video segments from DASH server. 

> This repository adapted from [Aljoby/Setup-Client-Server-DASH-video-streaming](https://github.com/Aljoby/Setup-Client-Server-DASH-video-streaming).

## Getting Started

All you need to run the DASH server and clients is [Docker](https://docs.docker.com).

### Install Docker

Please follow the instructions in the link to install the docker:

[docs.docker.com/get-docker/](https://docs.docker.com/get-docker/)

### DASH Server

1. Initialize the `apache2/httpd` container - the server

   ```bash
   sudo docker run -dit --name dash-server -p 80:80 -v `pwd`/dash/samples/dash-if-reference-player:/usr/local/apache2/htdocs/ httpd:2.4
   ```

   Now try to open [localhost](http://localhost) for verification. And if you are using Docker Desktop, you can see there is a docker container named `dash-server` running as follow:

   ![image-20200711170110399](https://img-upic.oss-accelerate.aliyuncs.com/uPic/2020-07/HNvXt9.png)

2. Stop the server

   ```bash
   sudo docker stop dash-server
   ```

   

3. Re-start the server

   ```
   sudo docker start dash-server
   ```

   

