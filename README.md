# README

Git with a cup of tea, painless self-hosted git service

## Usage

```sh
docker run --interactive --publish 3000:3000 --rm --tty timonier/gitea
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

If you like / use this project, please let me known by adding a [★](https://help.github.com/articles/about-stars/) on the [GitHub repository](https://github.com/timonier/nginx).

## Links

* [go-gitea](https://github.com/go-gitea/gitea)
* [image "timonier/gitea"](https://hub.docker.com/r/timonier/gitea/)
* [just-containers/s6-overlay](https://github.com/just-containers/s6-overlay)
* [jwilder/dockerize](https://github.com/jwilder/dockerize)
* [timonier/dumb-entrypoint](https://github.com/timonier/dumb-entrypoint)
