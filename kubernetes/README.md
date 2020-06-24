# Kubernetes Specifications

## Description

This folder consists of kubernetes specification files to create namespace, deploy demo-app and redis.

### Prerequisites:
I've already created the docker image of this go-lang application and pushed it to my public dockerhub registry.
If you create a new image locally, please change the name inside the demo-app-deployment.yaml accordingly and if its a private repository you might need to create a docker secret add ImagePullSecrets in the file.

### Steps to deploy these objects on Kubernetes clusters

- Create demo-ops namespace

  Command: kubectl apply -f demo-ops-ns.yaml

- Deploy redis deployment & service

  Command: kubectl apply -f redis-deployment.yaml

- Deploy demo-app deployment & service (which includes probes, resource quotas)

  Command: kubectl apply -f demo-app-deployment.yaml

### To Test this deployment

- Create test-demo-app deployment

  Command: kubectl apply -f test-demo-app-deployment.yaml

- Exec into the pod

  Command: kubectl exec -it <name-of-pod> /bin/sh -n demo-ops

- Execute Curl command

  Command: curl demo-app-svc

### Output
![Alt text](/output/kubernetes-output.jpg?raw=true "Kubernetes Deployment Output")
