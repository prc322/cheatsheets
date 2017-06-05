### Create app

```bash
$ heroku create MY_APP_NAME
```

### Add addons

```bash
$ heroku addons:create mongolab:sandbox
$ heroku addons:create heroku-redis:hobby-dev
```

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
$ heroku git:remote --remote REMOTE_NAME --app APP_NAME
```

### Batch delete apps with grep

```bash
$ heroku apps | grep review | while read line; do heroku apps:destroy -a $line --confirm=$line; done
```
