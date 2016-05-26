# `python.node`

This image is based off the [`python:3.5`](https://hub.docker.com/_/python/) image and
contains a `node.js` installation based off the official [docker image](https://hub.docker.com/_/node/).

The `onbuild` variant contains `onbuild` instruction to install `pip` and `npm` dependencies.

## Logging in to Gitlab Container Registry
Credentials are managed by `docker login`. Login with `docker login registry.gitlab.com`

## Building and pushing new images
Assuming that the Python version we want to build is `3.5` and the Node.js version is `6.1`, then we can build
the images as such:

```bash
docker build -t registry.gitlab.com/finnet-gds/python-node:3.5-6.1 .
docker push registry.gitlab.com/finnet-gds/python-node:3.5-6.1

docker build -t registry.gitlab.com/finnet-gds/python-node:3.5-6.1-onbuild onbuild/
docker push registry.gitlab.com/finnet-gds/python-node:3.5-6.1-onbuild
```

## Supported tags and respective `Dockerfile` links

- `3.5-6.1`: Python 3.5 with Node.js 6.1.0 ([Dockerfile](Dockerfile))
- `3.5-6.1-onbuild`: Python 3.5 with Node.js 6.1.0 with `ONBUILD` triggers ([Dockerfile](onbuild/Dockerfile))
