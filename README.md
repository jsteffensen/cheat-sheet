# heroku-cheat-sheet
---
##### Link dir to existing app:

`heroku git:remote -a project`

---
##### Enable labs:

`heroku labs:enable runtime-dyno-metadata`

```
HEROKU_APP_ID:                   9daa2797-e49b-4624-932f-ec3f9688e3da
HEROKU_APP_NAME:                 example-app
HEROKU_DYNO_ID:                  1vac4117-c29f-4312-521e-ba4d8638c1ac
HEROKU_RELEASE_VERSION:          v42
HEROKU_SLUG_COMMIT:              2c3a0b24069af49b3de35b8e8c26765c1dba9ff0
HEROKU_SLUG_DESCRIPTION:         Deploy 2c3a0b2
```
---
##### Enable exec:

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
