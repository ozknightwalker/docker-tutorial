# DOCKER TUTORIAL

## CREATING A DOCKER FILE

- create a file called `Dockerfile` to define a container

## BUILDING A DOCKER IMAGE

to build the image do a `docker build -t {tag} {directory of the Dockerfile}`

```
docker build -t friendlyhello .
```

so when you do `docker images`, `friendlyhello` image will be listed

## RUNNING A DOCKER IMAGE

to run the image do `docker run -p {port from}:{port forward} {image}`

```
docker run -p 4000:80 friendlyhello
```

you can add `-d` argument to run the docker container on the background

given that the `app.py` runs in port 80, 80 there is the port within the container
and not the whole system. so to be able to access it we need to map port 4000 to point to
the containers port 80. so when we visit `localhost:4000` it will access the newly running
docker container


## DOCKER CONTAINER

to list the containers

```
docker container ls
```

to stop a container/s

```
docker container stop {container ID}
```

to create a tag a container

```
# docker tag {image} {username}/{repository}:{tag}
docker tag friendlyhello jcdin/get-started:step-1
```


