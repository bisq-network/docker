# Bisq Docker

Building Bisq from source is currently a rather involved process, and this the Docker configuration here aims to make it much easier to get up and running with a Bisq development environment.

## Clone locally

    git clone https://github.com/bitsquare/docker.git && cd docker

## Build image

    sudo docker build -t bisq-0.5.2 .

## Run container

You may want to mount the bisq data directory on your host for easier upgrades

    sudo docker run -v $PWD/data:/root/.local/share/bisq -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY bisq-0.5.2

## Bisq data directory

When working with a development version of Bisq, it is important to use a different data directory than your personal "Production" version of Bisq. To avoid data loss, please read and follow the instructions in this document **carefully**: https://github.com/bitsquare/bitsquare/wiki/Switching-to-a-new-data-directory
