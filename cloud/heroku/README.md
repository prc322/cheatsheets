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
