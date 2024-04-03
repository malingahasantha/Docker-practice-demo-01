# Docker-practice-demo-01
Practice Docker Projects

Below are the commands run in terminal

docker ps

docker build -t hello-docker .

docker images

docker run -d -p8080:80 hello-docker

docker ps

docker stop 833611e99274

docker start 833611e99274

docker stop 833611e99274

docker start 833611e99274 --name hello_world_docker

  unknown flag: --name
  
  See 'docker start --help'.
  
docker rename busy_clarke hello_world_docker

docker start hello_world_docker

docker ps

CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS                  NAMES
833611e99274   hello-docker   "/docker-entrypoint.…"   4 minutes ago   Up 4 seconds   0.0.0.0:8080->80/tcp   hello_world_d

---------------------------------------------------------------------------------------------------------------

PS E:\DOCKER\Docker-practice-demo-01> docker ps

CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

PS E:\DOCKER\Docker-practice-demo-01>

PS E:\DOCKER\Docker-practice-demo-01> docker build -t hello-docker .

[+] Building 0.6s (7/7) FINISHED                                                                 docker:default

 => [internal] load build definition from Dockerfile                                                       0.1s
 
 => => transferring dockerfile: 88B                                                                        0.0s
 
 => [internal] load metadata for docker.io/library/nginx:latest                                            0.0s
 
 => [internal] load .dockerignore                                                                          0.1s
 => => transferring context: 2B                                                                            0.0s
 => [internal] load build context                                                                          0.1s
 => => transferring context: 288B                                                                          0.0s
 => CACHED [1/2] FROM docker.io/library/nginx:latest                                                       0.0s
 => [2/2] COPY index.html /usr/share/nginx/html                                                            0.1s
 => exporting to image                                                                                     0.1s
 => => exporting layers                                                                                    0.1s
 => => writing image sha256:6f2806f9d15a3646e0bccecd792f26d9959624418fec9f4b9bd62f3c15a46568               0.0s
 => => naming to docker.io/library/hello-docker                                                            0.0s

What's Next?
  View a summary of image vulnerabilities and recommendations → docker scout quickview
PS E:\DOCKER\Docker-practice-demo-01>
PS E:\DOCKER\Docker-practice-demo-01> docker images
REPOSITORY     TAG       IMAGE ID       CREATED          SIZE
hello-docker   latest    6f2806f9d15a   36 seconds ago   187MB
<none>         <none>    b841cfa86327   7 days ago       137MB
web_demo       v1        c622285631c7   9 days ago       187MB
node           latest    c3978d05bc68   11 days ago      1.1GB
ubuntu         latest    ca2b0f26964c   3 weeks ago      77.9MB
postgres       latest    b9390dd1ea18   4 weeks ago      431MB
nginx          1.25.4    92b11f67642b   5 weeks ago      187MB
nginx          latest    92b11f67642b   5 weeks ago      187MB
redis          latest    170a1e90f843   2 months ago     138MB
hello-world    latest    d2c94e258dcb   10 months ago    13.3kB
demo           latest    35c6c67ec35b   12 months ago    5.61MB
PS E:\DOCKER\Docker-practice-demo-01>
PS E:\DOCKER\Docker-practice-demo-01> docker run -d -p8080:80 hello-docker
833611e99274686ad12bb47ad979dc387b237fdc4feef01178f8dfacfb97a70c
PS E:\DOCKER\Docker-practice-demo-01>
PS E:\DOCKER\Docker-practice-demo-01> docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS                  NAMES        
833611e99274   hello-docker   "/docker-entrypoint.…"   6 seconds ago   Up 5 seconds   0.0.0.0:8080->80/tcp   busy_clarke  
PS E:\DOCKER\Docker-practice-demo-01>
PS E:\DOCKER\Docker-practice-demo-01> docker stop 833611e99274
833611e99274
PS E:\DOCKER\Docker-practice-demo-01> docker start 833611e99274
833611e99274
PS E:\DOCKER\Docker-practice-demo-01> docker stop 833611e99274
833611e99274
PS E:\DOCKER\Docker-practice-demo-01> docker start 833611e99274 --name hello_world_docker
unknown flag: --name
See 'docker start --help'.
PS E:\DOCKER\Docker-practice-demo-01> docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
PS E:\DOCKER\Docker-practice-demo-01> 
PS E:\DOCKER\Docker-practice-demo-01> docker rename busy_clarke hello_world_docker
PS E:\DOCKER\Docker-practice-demo-01> docker start hello_world_docker
hello_world_docker
PS E:\DOCKER\Docker-practice-demo-01> docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS                  NAMES
833611e99274   hello-docker   "/docker-entrypoint.…"   4 minutes ago   Up 4 seconds   0.0.0.0:8080->80/tcp   hello_world_docker
PS E:\DOCKER\Docker-practice-demo-01> 
