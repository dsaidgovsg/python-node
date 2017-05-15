# `python-node`

This image is based off the [`python:3.6`](https://hub.docker.com/_/python/) image and
contains a `node.js` installation based off the official [docker image](https://hub.docker.com/_/node/).

There is an additional Dockerfile for PyPy3.5 v5.7.

## Building and pushing new images
Assuming that the Python version we want to build is `3.5` and the Node.js version is `6.9.4`, then we can build
the images as such:

```bash
docker build -t python-node:3.6-6.10.3 .
docker push python-node:3.6-6.10.3
```

## Supported tags and respective `Dockerfile` links

- `3.5-6.9.4`: Python 3.5 with Node.js 6.9.4 ([Dockerfile](Dockerfile))
- `3.6-6.10.3`: Python 3.6 with Node.js 6.10.3 ([Dockerfile](Dockerfile))
- `pypy3-5-6.10.3`: PyPy3.5 v5.7 with Node.js 6.10.3 ([Dockerfile](Dockerfile))
