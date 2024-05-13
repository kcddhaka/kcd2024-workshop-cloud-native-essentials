**Table of Contents:**
- [1. Kubernetes Cluster Management Using Kind](#1-kubernetes-cluster-management-using-kind)
  - [1.1. Create a Kind Cluster](#11-create-a-kind-cluster)
  - [1.2. Create Kubernetes Cluster in CLI](#12-create-kubernetes-cluster-in-cli)
  - [1.3. Create Kubernetes in CLI Using a Config file](#13-create-kubernetes-in-cli-using-a-config-file)
  - [1.4. Create Ingress Ready Kubernetes Cluster Using Kind](#14-create-ingress-ready-kubernetes-cluster-using-kind)
  - [1.5. Delete a Kubernetes Cluster](#15-delete-a-kubernetes-cluster)
- [2. References](#2-references)
- [3. Appendix](#3-appendix)


# 1. Kubernetes Cluster Management Using Kind


## 1.1. Create a Kind Cluster

Pre-requisite:
- Start docker desktop service
- Install kind/kind.exe in your system based on host/guest operating system 

## 1.2. Create Kubernetes Cluster in CLI

In command, a kubernetes cluster can be created with below command.
```bash
# default cluster name is kind
kind create cluster

# with specific name for the cluster
kind create cluster --name dev
```

Now check the list of available cluster in your laptop:
```bash
% kind get clusters             
dev
kind
```

If you get an error message while creating a cluster then check the available cluster list and change your cluster name.
```bash
% kind create cluster 
ERROR: failed to create cluster: node(s) already exist for a cluster with the name "kind"
```


## 1.3. Create Kubernetes in CLI Using a Config file
[A sample config file for three node cluster](./kind-config1.yaml)

Now create your kubernetes cluster using `--config` flag.
```bash
kind create cluster --config kind-config1.yaml
```


## 1.4. Create Ingress Ready Kubernetes Cluster Using Kind


[Ingress Ready Kubernetes Cluster Using Kind](./kind-config-ingress-ready.yaml)

```bash
kind create cluster --config kind-config-ingress-ready.yaml
```

Ref:
- https://kind.sigs.k8s.io/docs/user/ingress/


## 1.5. Delete a Kubernetes Cluster

First, get list of available cluster in your laptop/pc:
```bash
% kind get clusters     
dev
kind
```

Now delete a kind cluster with a name arguments:
```bash
kind delete cluster --name dev
Deleting cluster "dev" ...
Deleted nodes: ["dev-control-plane"]
```

Now check cluster list again:
```bash
% kind get clusters                       
kind
```



# 2. References
- https://kind.sigs.k8s.io/docs/user/configuration/



# 3. Appendix
Logs from masOS:
```bash
aaa@hostmacOs kind % kind create cluster --config kind-config-ingress-ready.yaml
Creating cluster "kind" ...
 ✓ Ensuring node image (kindest/node:v1.29.2) 🖼
 ✓ Preparing nodes 📦 📦 📦  
 ✓ Writing configuration 📜 
 ✓ Starting control-plane 🕹️ 
 ✓ Installing CNI 🔌 
 ✓ Installing StorageClass 💾 
 ✓ Joining worker nodes 🚜 
Set kubectl context to "kind-kind"
You can now use your cluster with:

kubectl cluster-info --context kind-kind

Thanks for using kind! 😊
aaa@hostmacOs kind % 
```

Check cluster status:
```bash
aaa@hostmacOs kind % kubectl get node
NAME                 STATUS   ROLES           AGE   VERSION
kind-control-plane   Ready    control-plane   71s   v1.29.2
kind-worker          Ready    <none>          47s   v1.29.2
kind-worker2         Ready    <none>          48s   v1.29.2
aaa@hostmacOs kind % 
```

Check kubernetes cluster components:
```bash
% kubectl get pod --namespace kube-system
NAME                                         READY   STATUS    RESTARTS      AGE
coredns-76f75df574-7lmpr                     1/1     Running   1 (43m ago)   3d16h
coredns-76f75df574-pc28w                     1/1     Running   1 (43m ago)   3d16h
etcd-kind-control-plane                      1/1     Running   0             43m
kindnet-42jv9                                1/1     Running   1 (43m ago)   3d16h
kindnet-g6whb                                1/1     Running   1 (43m ago)   3d16h
kindnet-w2msq                                1/1     Running   1 (43m ago)   3d16h
kube-apiserver-kind-control-plane            1/1     Running   0             43m
kube-controller-manager-kind-control-plane   1/1     Running   1 (43m ago)   3d16h
kube-proxy-74v7b                             1/1     Running   1 (43m ago)   3d16h
kube-proxy-j9ms2                             1/1     Running   1 (43m ago)   3d16h
kube-proxy-lf664                             1/1     Running   1 (43m ago)   3d16h
kube-scheduler-kind-control-plane            1/1     Running   1 (43m ago)   3d16h
```