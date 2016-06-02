Lets you fetch the git revision hash used to build the app from the `GIT_REV`

## requirements

- dokku 0.4.0+
- docker 1.8.x

## installation

```shell
dokku plugin:install https://github.com/Anadea/dokku-git-rev.git dokku-git-rev
```

## hooks

This plugin provides hooks:

* `post-release-buildpack`: adds the `GIT_REV` env var
* `post-release-dockerfile`: adds the `GIT_REV` env var
* `receive-app`: captures the current `GIT_REV`

## usage

On git deploys, the `GIT_REV` environment variable will be set in `/app/.profile.d/git_rev.sh` and be available for your usage.

## thanks

- nornagon who made the initial plugin (albeit it was not really working) - this plugin is built upon his work (https://github.com/nornagon/dokku-git-rev)
- mlebkowski/puck who helped me out and made the initial verison of the receive-app based version. I based this version upon that idea and made it bug free and more stable (https://github.com/mlebkowski/dokku-git-rev/tree/fix/first-push)
- cjblomqvist
