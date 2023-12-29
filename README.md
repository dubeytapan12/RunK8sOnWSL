# RunK8sOnWSL
# Kubectl Installation
Detailed steps to run K8s on Windows WSL ubunutu sub system using minikube.

**Execute Below command to install Kubectl , Open WSL ubunut terminal and Execute below command**
```
$ curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
```
**Execute below command to change the permissions of a file. In this case, +x grants execute permission to the kubectl binary.**
``` 
$ chmod +x ./kubectl 
```

**Execute below Command It moves the kubectl binary from the current directory (./kubectl) to the directory /usr/local/bin with the name kubectl.**

```
$ sudo mv ./kubectl /usr/local/bin/kubectl
```
**Execute below Command to verify installation**
```
$ kubectl version --client
```
# Minikube Installation

** Execute Below Command to download minikube binary **
```
$ curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```
**Execute Below Command to Install minikube**
```
$ sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

Now Just Execute  ``` Minikube start ``` to start minikube and  ``` kubectl cluster-info ``` to view k8s cluster. 
