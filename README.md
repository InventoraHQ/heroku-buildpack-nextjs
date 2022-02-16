# heroku-buildpack-monorepo-cleaner

This buildpack is intended to allow a monorepo to remove unrelated code folders to reduce bundle size

```
heroku buildpacks:add "https://github.com/InventoraHQ/heroku-buildpack-monorepo-cleaner" -a yourappname
heroku buildpacks:set --index 1 "heroku/node" -a yourappname
heroku config:set REMOVE_DIR="some_folder some_other_folder" -a yourappname

```

**Note:** This should be the first buildpack, so it precedes any `yarn install` or similar.

