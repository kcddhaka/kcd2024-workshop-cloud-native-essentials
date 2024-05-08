**Table of Contents:**
- [1. Workshop: Cloud Native Essentials for Beginners](#1-workshop-cloud-native-essentials-for-beginners)
- [2. Install Docker Desktop](#2-install-docker-desktop)
- [3. Install Kind](#3-install-kind)
- [4. Create a Kubernetes Cluster](#4-create-a-kubernetes-cluster)
- [5. Entend Kubernetes Cluster Capabilites](#5-entend-kubernetes-cluster-capabilites)
  - [5.1. MetalLB](#51-metallb)
  - [5.2. Ingress](#52-ingress)
  - [5.3. Kubernetes Gateway](#53-kubernetes-gateway)
  - [5.4. Service Mesh - Istio](#54-service-mesh---istio)
- [6. Observability](#6-observability)
  - [6.1. Logging](#61-logging)
  - [6.2. Monitoring](#62-monitoring)
  - [6.3. Tracing](#63-tracing)
- [7. References](#7-references)


# 1. Workshop: Cloud Native Essentials for Beginners

A number of lightweight tools are available that support a [Kubernetes](https://kubernetes.io/) cluster on top of a container platform like Docker, Podman, etc.

- [Kind](https://kind.sigs.k8s.io/)
- [k3s](https://k3s.io/) / [K3d](https://k3d.io/v5.6.3/)


# 2. Install Docker Desktop

[Follow me to install docker desktop](./installation/docker-desktop/install-docker-desktop.md)


# 3. Install Kind 

- [Kind Installation](./installation/kind/kind-installation.md)

# 4. Create a Kubernetes Cluster

- [Kind Cluster Management](./installation/kind/kind-cluster-management.md)



# 5. Entend Kubernetes Cluster Capabilites

## 5.1. MetalLB

## 5.2. Ingress

Ref:
- https://medium.com/groupon-eng/loadbalancer-services-using-kubernetes-in-docker-kind-694b4207575d


## 5.3. Kubernetes Gateway

## 5.4. Service Mesh - Istio


# 6. Observability

## 6.1. Logging
- [Install Elastic Cloud on Kubernetes](./installation/elastic-cloud/elastic-cloud-kubernetes-installation.md)
- [Install Fluent-bit](./installation/fluent-bit/fluent-bit-installation.md)

## 6.2. Monitoring
- [Prometheus Operator Deployment](./installation/prometheus/prometheus-install.md)


## 6.3. Tracing






# 7. References
- https://docs.docker.com/get-docker/
- https://docs.docker.com/desktop/install/windows-install/
- https://kind.sigs.k8s.io/docs/user/using-wsl2/