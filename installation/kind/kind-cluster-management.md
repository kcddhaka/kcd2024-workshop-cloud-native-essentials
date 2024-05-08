**Table of Contents:**
- [1. Kubernetes Cluster Management Using Kind](#1-kubernetes-cluster-management-using-kind)
  - [1.1. Create a Kind Cluster](#11-create-a-kind-cluster)
  - [1.2. Create Kubernetes Cluster in CLI](#12-create-kubernetes-cluster-in-cli)
  - [1.3. Create Kubernetes in CLI Using a Config file](#13-create-kubernetes-in-cli-using-a-config-file)
- [2. References](#2-references)


# 1. Kubernetes Cluster Management Using Kind


## 1.1. Create a Kind Cluster

Pre-requisite:
- Start docker desktop service
- Install kind/kind.exe in your system 

## 1.2. Create Kubernetes Cluster in CLI

In command, a kubernetes cluster can be created with below command.
```bash
kind create cluster
```

## 1.3. Create Kubernetes in CLI Using a Config file
[A sample config file for three node cluster](./kind-config1.yaml)

Now create your kubernetes cluster using `--config` flag.
```bash
kind create cluster --config kind-config1.yaml
```

# 2. References
- https://kind.sigs.k8s.io/docs/user/configuration/