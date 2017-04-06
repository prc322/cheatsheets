### Scaling dynos

```bash
$ heroku ps:scale web=1
$ heroku ps:scale worker=1
```

### Connecting to logs

```bash
$ heroku logs --tail
```

### Add git remote

```bash
$ heroku git:remote -a APP_NAME
```

### Batch delete apps with grep

```bash
$ heroku apps | grep review | while read line; do heroku apps:destroy -a $line --confirm=$line; done
```
