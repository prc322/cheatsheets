# docker

### Pull an image

```bash
$ docker pull ubuntu
```

### Start container from image

```bash
# -t opens a terminal session within the container
# -i keeps the STDIN open so we can read from and write to it
# --rm removes the container after it exists
$ docker run --rm -it ubuntu/amazing-things
```

### Start container with custom entry point and arguments

```bash
# runs the exec /bin/bash instead of the container entry point
# and uses "/root/myscript.sh" as parameter
docker run --rm --entrypoint /bin/bash ubuntu/entry /root/myscript.sh
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