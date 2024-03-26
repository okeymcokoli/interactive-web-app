# interactive-web-app
how to deploy a web application with its database on local Kubernetes cluster

how to deploy a web application with its database into a local Kubernetes cluster

This repository contains a simple step for deploying an interractive web application with MongoDB using docker, minikube, and kubernetes on your localhost with port 3000 exposed.  

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Endpoints](#endpoints)
- [Contributing](#contributing)
- [Credits](#contibutors)

### Prerequisites

- Active Terminal
- Code Editor
- Installed minikube and Kubectl -(see instructions below)
- Installed Docker Desktop  -(see instructions below)

### Getting Started

1. Install Docker desktop - https://www.docker.com/products/docker-desktop/

2. run docker --version to confirm successful installation
```
docker --version
```
3. Install minikube - https://kubernetes.io/docs/tasks/tools/#kubectl

4. run minikube version to confirm successful installation
```
minikube version
```

5. Clone the repository:
   git clone https://github.com/okeymcokoli/interactive-web-app.git

6. Configure the following files to suite your environment or use as provided.

    a. mongo-config.yaml
    b. mongo-secret.yaml
    c. mongo.yaml
    d. webapp.yaml

7. start minikube using the virtual machine driver hyperkit
```
minikube start --vm-driver=hyperkit 
minikube status
```

8. Verify minikube node's ip address
```
minikube ip
kubectl describe svc
```

### Endpoints
9. access your application using minikubeIP:NodePort http://http://10.244.0.15:3000


####PS: If you can't access the NodePort service webapp with MinikubeIP:NodePort, execute the following command:

```
minkube service webapp-service
```

10. stop minikube cluster
```
minikube stop
```

### Credits
11. Big shoutout to Nana Janashia and Adekunle Flourish whose insights and codes were curled for this project

## Contributing
Contributions are welcome! Feel free to open issues, submit pull requests, or provide suggestions to improve this project.


