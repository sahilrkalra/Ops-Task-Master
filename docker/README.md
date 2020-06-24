# Dockerfile to create Docker Image

## Description

This folder consists of the sample go app and the Dockerfile to create a docker image out of it.

### Steps to create the docker image

- docker build -t {dockerImageName} .

Replace {dockerImageName} with the actual name of the image

- docker push {dockerImageName}

Replace {dockerImageName} with the actual name of the image you want to push to the registry.
