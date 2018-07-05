# Travis CI CLI
[![CircleCI](https://circleci.com/gh/MaSpeng/docker-hub-travis-cli/tree/master.svg?style=svg)](https://circleci.com/gh/MaSpeng/docker-hub-travis-cli/tree/master) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/cd267fb46f544ea0abe80a63e43cb592)](https://www.codacy.com/app/marco.spengler/docker-hub-travis-cli?utm_source=github.com&utm_medium=referral&utm_content=MaSpeng/docker-hub-travis-cli&utm_campaign=Badge_Grade)

This docker image includes the command line client to interact with a Travis CI service. It works with [travis-ci.org](https://travis-ci.org), [travis-ci.com](https://travis-ci.com) or any custom Travis CI setup you might have.

## Supported tags and respective Dockerfile links
* `1.8`, `latest` [(1.8/Dockerfile)](https://github.com/maspeng/docker-hub-travis/blob/master/1.8/Dockerfile)

## How to use this image
To use the `Travis cli` you can do the following.

```bash
$ docker run \
    --rm \
    --interactive \
    --tty \
    --volume "$(pwd)":/app \
    maspeng/travis-cli
```

You can mount the Travis home directory from your host inside the Container to share caching and configuration files:

```bash
$ docker run \
    --rm \
    --interactive \
    --tty \
    --volume ~/.travis:/root/.travis \
    --volume "$(pwd)":/app \
    maspeng/travis-cli
```

## Quick reference
* **Where to get help:**
[the Docker Community Forums](https://forums.docker.com), [the Docker Community Slack](https://blog.docker.com/2016/11/introducing-docker-community-directory-docker-community-slack), or [Stack Overflow](https://stackoverflow.com/search?tab=newest&q=docker)

* **Where to file issues:**
https://github.com/maspeng/docker-hub-travis-cli/issues

* **Maintained by:**
[MaSpeng](https://github.com/MaSpeng)

* **Source of this description:**
[Repository README.md](https://github.com/maspeng/docker-hub-travis-cli/blob/master/README.md)
