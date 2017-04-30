# hg-circle-base

Base docker image used by our CircleCI builds

# Supported images

1. [`hugoai/node`](https://hub.docker.com/r/hugoai/node/) - Base image for node.js based projects.

# Considerations

* The base image is uploaded to the **public** docker repo, [Docker Hub](https://hub.docker.com). Please do not include business sensitive info/code in the base image!
** *Why is this? It drastically simplifies CircleCI permissions.*
* If you want something to update on the build of a dervied image, eg. a service, then please use the [`ONBUILD` instruction](https://docs.docker.com/engine/reference/builder/#onbuild).

# Docker Hub Organization

We have the [`hugoai`](https://hub.docker.com/u/hugoai/) organization on Docker Hub, if you need to add more images please request to join this.
