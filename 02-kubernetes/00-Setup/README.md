# Setup K8s Kind Cluster

## Install the Kind & Other Utils 
```
sh install-k8s.sh 
```

## Now bring up Kind Cluster
```
kind create cluster --config cluster-mainfest.yml
```

## Node Status 
```
kubectl get nodes 
```


