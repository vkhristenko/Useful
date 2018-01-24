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

## Tag the image
```
docker tag <image-id> <username>/<repository>:<tag>
```
