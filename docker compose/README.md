# Docker-Compose File

## Description

This folder consists of docker-compose.yml file to deploy both the containers : demo-app and redis.

### Prerequisites:
Docker & Docker-compose should be already installed on the machine.
I've already created the docker image of this go-lang application and pushed it to my public dockerhub registry.
If you create a new image locally, please change the name inside the docker-compose.yml accordingly

### Steps to execute this docker-compose.yml file

- Execute docker-compose.yml file
Command: docker-compose up -d

- Test the application by executing the following command on the same machine where both the containers deployed by docker-compose.yml are running.
Command: curl localhost:8000

### Output:
![Alt text](/output/docker-compose-output.jpg?raw=true "Docker Compose Output")
