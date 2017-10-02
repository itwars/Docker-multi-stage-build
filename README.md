# An example of Docker multi-stage building with Golang

## Introduction

This repository is part of my blog post on [Docker multistage builds](http://www.it-wars.com/posts/virtualisation/docker-multi-stage-builds/).

## Howto Docker multistage builds

To illustrate this purpose, I use a small *golang app* that write ascii colored output. It use a lib + a local package call myframe.go.

In the **Dockerfile**, *first stage build* the golang app binary, while *second stage copy* it into the final image for run purpose.

## Bonus

As we produce a binary, I can make the second stage using the magic **FROM scratch** that allowed me to make a 2Mb **tiny Docker image**!
