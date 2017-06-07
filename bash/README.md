### Search recursively for a string in files

```bash
$ find . -type f -print0 | xargs -0 grep -l "what you want to find"
```
