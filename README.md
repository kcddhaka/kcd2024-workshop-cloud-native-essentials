**Table of Contents:**
- [1. Workshop: Cloud Native Essentials for Beginners](#1-workshop-cloud-native-essentials-for-beginners)
- [2. Install Docker Desktop](#2-install-docker-desktop)
- [3. Install Kind](#3-install-kind)
- [4. Create a Kubernetes Cluster](#4-create-a-kubernetes-cluster)
- [5. Kuberenetes Applications](#5-kuberenetes-applications)
- [6. Entend Kubernetes Cluster Capabilites](#6-entend-kubernetes-cluster-capabilites)
  - [6.1. MetalLB](#61-metallb)
  - [6.2. Ingress](#62-ingress)
  - [6.3. Kubernetes Gateway](#63-kubernetes-gateway)
  - [6.4. Service Mesh - Istio](#64-service-mesh---istio)
- [7. Observability](#7-observability)
  - [7.1. Logging](#71-logging)
  - [7.2. Monitoring](#72-monitoring)
  - [7.3. Tracing](#73-tracing)
  - [7.4. Telemetry](#74-telemetry)
- [8. Build Container Apllication from Source Code](#8-build-container-apllication-from-source-code)
- [9. CNCF Certification](#9-cncf-certification)
- [10. References](#10-references)


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


# 5. Kuberenetes Applications
- [Kuberenetes Applications](./docs/kubernetes-applications/README.md)
  - [A Simple Web Application Server in Kubernetes](./docs/kubernetes-applications/first-simple-application/README.md)


# 6. Entend Kubernetes Cluster Capabilites

## 6.1. MetalLB

Ref: 
- https://metallb.universe.tf/

## 6.2. Ingress

Ref:
- https://medium.com/groupon-eng/loadbalancer-services-using-kubernetes-in-docker-kind-694b4207575d


## 6.3. Kubernetes Gateway

Ref:
- https://gateway-api.sigs.k8s.io/


## 6.4. Service Mesh - Istio
Ref:
- https://istio.io/

# 7. Observability

## 7.1. Logging
- [Install Elastic Cloud on Kubernetes](./installation/elastic-cloud/elastic-cloud-kubernetes-installation.md)
- [Install Fluent-bit](./installation/fluent-bit/fluent-bit-installation.md)

## 7.2. Monitoring
- [Prometheus Operator Deployment](./installation/prometheus/prometheus-install.md)


## 7.3. Tracing

Ref:
- https://www.jaegertracing.io/


## 7.4. Telemetry

Ref:
- https://opentelemetry.io/


# 8. Build Container Apllication from Source Code

- [Build a simple application](./docs/build-container-application/README.md)


# 9. CNCF Certification

- Kubernetes and Cloud Native Associate (KCNA)
- Kubernetes and Cloud Security Associate (KCSA)
- Certified Kubernetes Administrator (CKA)
- Certified Kubernetes Application Developer (CKAD)
- Certified Kubernetes Security Specialist (CKS)

Ref:
- https://www.cncf.io/training/certification/




# 10. References
- https://docs.docker.com/get-docker/
- https://docs.docker.com/desktop/install/windows-install/
- https://kind.sigs.k8s.io/docs/user/using-wsl2/
- https://landscape.cncf.io/
- https://www.cncf.io/training/certification/