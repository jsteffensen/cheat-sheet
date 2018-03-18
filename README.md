# Maven
Start project from scratch with package com.c2_systems.app containing App.java with public static void main( String[] args ):
`mvn -B archetype:generate -DarchetypeGroupId=org.apache.maven.archetypes -DgroupId=com.c2_systems.app -DartifactId=my-app`

# Heroku

## Link dir to existing app:

`heroku git:remote -a [project]`

## Enable labs:

`heroku labs:enable runtime-dyno-metadata`

```
HEROKU_APP_ID:                   9daa2797-e49b-4624-932f-ec3f9688e3da
HEROKU_APP_NAME:                 example-app
HEROKU_DYNO_ID:                  1vac4117-c29f-4312-521e-ba4d8638c1ac
HEROKU_RELEASE_VERSION:          v42
HEROKU_SLUG_COMMIT:              2c3a0b24069af49b3de35b8e8c26765c1dba9ff0
HEROKU_SLUG_DESCRIPTION:         Deploy 2c3a0b2
```

## Enable exec:

`heroku ps:exec`

then

`git commit -m "Heroku Exec" --allow-empty`

`git push`

then deploy app from  dashboard.
When app is running, repeat:

`heroku ps:exec`

to see number of cores when in  exec mode:

`grep -c processor /proc/cpuinfo`

---
# Git

## Initialise a local project:
Create repo via webinterface an copy url.
then go to terminal:

Initialise:
`git init`

Add files:
`git add .`

Commit:
`git commit -m "initial commit"`

Set remote:
`git remote add origin [repo url]`

Verify url:
`git remote -v`

Push to remote (wiping existing commit-history from display):
`git push -u --force origin master`

## Reset to previous SHA commit:
`git reset --hard [previous Commit SHA id here]`
`git push origin master -f`
