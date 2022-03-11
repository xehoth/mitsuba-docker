# mitsuba-docker

[![CI](https://github.com/xehoth/mitsuba-docker/actions/workflows/docker-image.yml/badge.svg)](https://github.com/xehoth/mitsuba-docker/actions/workflows/docker-image.yml)

Dockerfile for [mitsuba renderer 0.6](https://github.com/mitsuba-renderer/mitsuba).  
Build with `ubuntu:latest` (ubuntu 20.04).

## From Docker Hub

You can directly use the image published on [docker hub](https://hub.docker.com/repository/docker/xehoth/mitsuba)

```shell
docker pull xehoth/mitsuba
```

## Build

```shell
docker build -t your_image_name .
```

## Run with WSLg

You can forward X11 to suppuort `mtsgui`.

```
docker run -it --name "mitsuba" --network host --gpus=all -v /tmp/.X11-unix/:/tmp/.X11-unix -e DISPLAY xehoth/mitsuba /bin/bash
```
