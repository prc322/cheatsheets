# docker

### Create a docker-machine on AWS at the eu central region

```bash
$ docker-machine create --driver amazonec2 --amazonec2-region eu-central-1 my-aws-vm
```

### Pull an image

```bash
$ docker pull ubuntu
```

### Start container from image

```bash
# -t opens a terminal session within the container
# -i keeps the STDIN open so we can read from and write to it
# --rm removes the container after it exits
# -p 8080:80 binds the hosts' port 8080 to the containers' port 80
$ docker run --rm -it -p 8080:80 ubuntu/amazing-things
```

### Start container with custom entry point and arguments

```bash
# runs the exec /bin/bash instead of the container entry point
# and uses "/root/myscript.sh" as parameter
docker run --rm --entrypoint /bin/bash ubuntu/entry /root/myscript.sh
```

### Mount a folder of the host system

```bash
# /var/dev is a path on the hosts' filesystem
# /dev is the mounted path within the container
docker run -it --rm -v /var/dev/:/dev ubuntu/review
```

### Run executables inside a container

```bash
docker exec keen_wilson /bin/bash -c "ls -l /root"
```

### Show images

```bash
$ docker images
```

### Show containers

```bash
# -a shows all containers, not just running ones
$ docker ps -a
```

### Clean up unused containers, networks, images, etc

```bash
$ docker system prune -f
```

### Save current state of container as image

```bash
$ docker commit 250782f08d6a
```

### Tag image

```bash
$ docker tag bcb09f5490383b7d2a2206653b1e19cfbc018a1284fb22b96ccdd9e5dfbaecc0 ubuntu/mine:v3
```

### Remove image

```bash
$ docker image rm 250782f08d6a
```
