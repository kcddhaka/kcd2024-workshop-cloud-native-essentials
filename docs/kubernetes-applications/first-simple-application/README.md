# First Simple Web Application Server in Kubernetes Cluster

First create a yaml defintion file for a nginx webserver.
```bash
kubectl run web --name nginx --dry-run=client -o yaml > web.yaml
```

Now create nginx web server in kubernetes cluster:
```bash
kubectl create -f web.yaml
```

Now check status of created web application:
```bash
kubectl get pod
```

Now a create service defintion file in yaml:
```bash
kubectl expose pod web --port 80 --dry-run=client -o yaml > web-svc.yaml
```

Now create kubernetes service for the created application:
```bash
kubectl create -f web-svc.yaml
```

Now check service and endpoint of created web application:
```bash
# check service
kubectl get svc

# check endpoint
kubectl get ep
```



# References
- https://kubernetes.io/docs/reference/kubectl/cheatsheet/
- https://kubernetes.io/docs/tasks/manage-kubernetes-objects/imperative-command/
- https://kubernetes.io/docs/tasks/manage-kubernetes-objects/imperative-config/
- https://kubernetes.io/docs/tasks/manage-kubernetes-objects/declarative-config/