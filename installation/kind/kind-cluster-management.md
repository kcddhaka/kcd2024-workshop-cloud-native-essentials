**Table of Contents:**
- [1. Kubernetes Cluster Management Using Kind](#1-kubernetes-cluster-management-using-kind)
  - [1.1. Create a Kind Cluster](#11-create-a-kind-cluster)
  - [1.2. Create Kubernetes Cluster in CLI](#12-create-kubernetes-cluster-in-cli)
  - [1.3. Create Kubernetes in CLI Using a Config file](#13-create-kubernetes-in-cli-using-a-config-file)
  - [Create Ingress Ready Kubernetes Cluster Usinf Kind](#create-ingress-ready-kubernetes-cluster-usinf-kind)
- [2. References](#2-references)
- [Appendix](#appendix)


# 1. Kubernetes Cluster Management Using Kind


## 1.1. Create a Kind Cluster

Pre-requisite:
- Start docker desktop service
- Install kind/kind.exe in your system 

## 1.2. Create Kubernetes Cluster in CLI

In command, a kubernetes cluster can be created with below command.
```bash
kind create cluster
kind create cluster --name dev
```

## 1.3. Create Kubernetes in CLI Using a Config file
[A sample config file for three node cluster](./kind-config1.yaml)

Now create your kubernetes cluster using `--config` flag.
```bash
kind create cluster --config kind-config1.yaml
```


## Create Ingress Ready Kubernetes Cluster Usinf Kind


[Ingress Ready Kubernetes Cluster Using Kind](./kind-config-ingress-ready.yaml)

```bash
kind create cluster --config kind-config-ingress-ready.yaml
```

Ref:
- https://kind.sigs.k8s.io/docs/user/ingress/



# 2. References
- https://kind.sigs.k8s.io/docs/user/configuration/



# Appendix
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
aaa@hostmacOs kind % k get node
NAME                 STATUS   ROLES           AGE   VERSION
kind-control-plane   Ready    control-plane   71s   v1.29.2
kind-worker          Ready    <none>          47s   v1.29.2
kind-worker2         Ready    <none>          48s   v1.29.2
aaa@hostmacOs kind % 
```