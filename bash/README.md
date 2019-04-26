### Search recursively for a string in files

```bash
$ find . -type f -print0 | xargs -0 grep -l "what you want to find"
```

### Rename files based on creation date

```bash
$ for f in *.mp4; do mv -- "$f" "$(date -r "$f" +%Y_%m_%d-%H_%M.mp4)"; done
```

### Do something for each line of an output

```bash
for image $(docker images -q);
do
  docker image rm $image
done
```
