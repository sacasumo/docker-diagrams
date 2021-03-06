# docker-diagrams

"Forked" from https://github.com/gtramontina/docker-diagrams

#### _Authenticate docker client with Github packages docker registry:_

Reference - https://docs.github.com/en/free-pro-team@latest/packages/using-github-packages-with-your-projects-ecosystem/configuring-docker-for-use-with-github-packages

Create a personal access token, with `read:packages` permissions. Drop it somewhere on your machine, such as `~/.github/docker-token`

before you pull, login to the registry:

```cat ~/.github/docker-token | docker login https://docker.pkg.github.com -u <username> --password-stdin```

#### _Running:_

```
$ cat example.py | docker run -i --rm -v $(pwd)/out:/out docker.pkg.github.com/stv-io/docker-diagrams/docker-diagrams:v0.20.0
```

The `/out` directory is where `diagram` will generate your PNGs.
