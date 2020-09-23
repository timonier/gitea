# README

Git with a cup of tea, painless self-hosted git service

⚠️ This project is no longer maintained. ⚠️

## Usage

```sh
docker run --interactive --publish 3000:3000 --rm --tty timonier/gitea
```

__Note__: By default `gitea` opens port `3000`.

It is possible to change `UID` and / or `GID` of user `git` (user used to run `gitea`) with environment variables `GITEA_UID` and `GITEA_GID`:

```sh
docker run --env GITEA_GID=1005 --env GITEA_UID=1005 --interactive --publish 3000:3000 --rm --tty timonier/gitea
```

It is possible to run a container in `read-only` mode if you mount the following folders:
* `/etc` if you want to change `UID` or `GID` of user `git`.
* `/run` and `/var/lib/gitea`.

__Note__: `/run` can be mount as `tmpfs`. In that case, `/run` must have flag `exec`.

```sh
# If you do not want to change "UID" or "GID" of user "git"

docker run --interactive --publish 3000:3000 --read-only --rm --tmpfs /run:exec --tty --volume $PWD/data:/var/lib/gitea timonier/gitea

# If you want to change "UID" or "GID" of user "git"

docker run --env GITEA_GID=1005 --env GITEA_UID=1005 --interactive --publish 3000:3000 --read-only --rm --tmpfs /run:exec --tty --volume /etc --volume $PWD/data:/var/lib/gitea timonier/gitea
```

## Links

* [go-gitea](https://github.com/go-gitea/gitea)
* [image "timonier/gitea"](https://hub.docker.com/r/timonier/gitea/)
* [just-containers/s6-overlay](https://github.com/just-containers/s6-overlay)
* [jwilder/dockerize](https://github.com/jwilder/dockerize)
* [timonier/dumb-entrypoint](https://gitlab.com/timonier/dumb-entrypoint)
