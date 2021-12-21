# 2048 Dockerized

Optimized dockerization of the famous game 2048 developer by @gabrielecirulli (https://github.com/gabrielecirulli/2048).

The construction is done in two steps - Multi-stage (https://docs.docker.com/develop/develop-images/multistage-build/), the first is based on a Ubi8 image which downloads and cleans the @gabrielecirulli repository (https://github.com/gabrielecirulli/2048). 

The second step, copies the necessary files from the first and is ready for execution.

## Docker build

`docker build -t 2048-dockerized:latest -f Dockerfile-2048 .`

## Docker run

`docker run -d -p 8080:80 2048-dockerized`