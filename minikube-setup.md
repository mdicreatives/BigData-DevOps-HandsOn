
### System is up to date(repositories are fine!)
```
sudo apt update
 ```
```
sudo apt upgrade
```

# Setup MiniKube (linux VM)
Setup local kubernetes cluster for this exercise i'll be using ```linux Virtual Machine``` running in virtualbox, i would suggest to follow along side me and use the similar setup or try ```da vinci people``` approach and try it out in your environment(windows,mac) the purpose is to just enjoy whatever approach you take!


Visit https://minikube.sigs.k8s.io


### Steps 

1. Go to https://minikube.sigs.k8s.io/docs/start/
2. Describe the target platform based on architecture you are using, in our case it will be 
    - Linux
    - x86-64
    - Stable
    - Debian package
3. The site will automatically provide the below commands based on architecture options selected, for example in our case:
    To install the latest minikube stable release on x86-64 Linux using Debian package:

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb


sudo dpkg -i minikube_latest_amd64.deb
```

After setup is complete, Run the cluster start command in my case i'm using docker as the driver but you can refer to official documentation drivers page for different options available:
```
minikube start --drive=docker
```
Check and confirm if minikube cluster is up and running:
```
minikube status
minikube kubectl -- get po -A
```

Some basic operation commands to interact with minikube:
```
# List profiles
minikube profile list

# Pause minikube
minikube pause

# Unpause minikube
minikube unpause

# Cluster Halt
minikube stop

# Delete all minikube clusters
minikube delete -all

```

## Spin Up Kubernetes UI
```
minikube dashboard
```

