### install hyperhit and minikube

`brew update`

`brew install hyperkit`

`brew install minikube`

`kubectl`

`minikube`

### create minikube cluster

`minikube start --vm-driver=hyperkit`

`kubectl get nodes`

`minikube status`

`kubectl version`

### delete cluster and restart in debug mode

`minikube delete`

`minikube config set driver {hyperv|virtualbox|hyperkit} --v=7 --alsologtostderr`

or

`minikube start --vm-drive={hyperv|virtualbox|hyperkit} --v=7 --alsologtostderr`

`minikube status`

### kubectl commands

`kubectl get nodes`

`kubectl get pod`

`kubectl get services`

`kubectl create deployment nginx-depl --image=nginx`

`kubectl get deployment`

`kubectl get replicaset`

`kubectl edit deployment nginx-depl`

### debugging

`kubectl logs {pod-name}`

`kubectl exec -it {pod-name} -- bin/bash`

### create mongo deployment

`kubectl create deployment mongo-depl --image=mongo`

`kubectl logs mongo-depl-{pod-name}`

`kubectl describe pod mongo-depl-{pod-name}`

### delete deplyoment

`kubectl delete deployment mongo-depl`

`kubectl delete deployment nginx-depl`

### create or edit config file

`vim nginx-deployment.yaml`

`kubectl apply -f nginx-deployment.yaml`

`kubectl get pod`

`kubectl get deployment`

### delete with config

`kubectl delete -f nginx-deployment.yaml`
