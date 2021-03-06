### Create app

```bash
$ heroku create MY_APP_NAME
```

### Add addons

```bash
$ heroku addons:create mongolab:sandbox
$ heroku addons:create heroku-redis:hobby-dev
```

### Set config variables

```bash
$ heroku config:set API_URL=http://api238.herokuapps.com
```

### Create a pipeline
```bash
# you need at least one app to create a pipeline
$ heroku pipelines:create PIPELINE_NAME -a APP_NAME -s production
```

### Add app to pipeline
```bash
$ heroku pipelines:add PIPELINE_NAME -a APP_NAME -s staging
```

### Add a domain to an app and wait for it

```bash
$ heroku domains:add app.example.io --app app-18406
$ heroku domains:wait 'app.example.io' --app app-18406
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

### Push current git branch to Heroku master

```bash
$ git push heroku +HEAD:master
```
