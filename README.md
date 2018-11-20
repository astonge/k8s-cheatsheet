# Kubectl Cheatsheet

Cluster -> Nodes -> Pods -> {Apps,Volumes}

* kubectl get - list resources
* kubectl describe - show detailed information about a resource
* kubectl logs - print the logs from a container in a pod
* kubectl exec - execute a command on a container in a pod

## Cluster info
```kubectl cluster-info```

## Get all
```kubectl get all```

## Get pods
```kubectl get pods```

## Get pod name
```export POD_NAME=$(kubectl get pods -o go-template --template '{{range .items}}{{.metadata.name}}{{"\n"}}{{end}}')```

## Get logs
```kubectl logs $POD_NAME```

## Run cmd on pod
```kubectl exec $POD_NAME env```

## Get shell on pod
```kubectl exec -ti $POD_NAME bash```
