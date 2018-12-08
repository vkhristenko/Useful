# Docker Commands

## Run hello-world
```
docker run hello-world
```

## List images
```
docker images
```

## List Running Containers
```
docker container ls
```

## Run with Swarm 
```
docker swarm init

docker stack deploy -c docker-compose.yml <name-to-use>
```

## Build a docker container image given a Dockerfile
- `test` is the image name to use
- `Dockerfile` should be present in directory `.` 
```
docker build -t test .
```

## Running the image 
- run by mapping port 80 within the container to port 4000 on the host machine
```
docker run -p 4000:80 test
```

- run in a detached mode
```
docker run -d -p 4000:80 test
```

- run a cc7 in an interactive shell 
```
docker run -it <image> /bin/bash
```

## Tag the image
```
docker tag <image-id> <username>/<repository>:<tag>
```

## Join a running container within another shell
```
docker exec -it b7327326d0da /bin/bash
```

## Remove stopped containers
**Will remove the image from disk (host filesystem)**
```
docker rm -f <container id>
```

## share a local directory `volume`
```
docker run -v /host/dir:/shared/dir -it 3e50fe78bedc /bin/bash
```
