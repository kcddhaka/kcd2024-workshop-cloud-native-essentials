**Table of Contents:**
- [1. Workshop: Cloud Native Essentials for Beginners](#1-workshop-cloud-native-essentials-for-beginners)
- [2. Install Docker Desktop](#2-install-docker-desktop)
- [3. Install Kind](#3-install-kind)
- [4. Create a Kubernetes Cluster](#4-create-a-kubernetes-cluster)
- [5. Kuberenetes Applications](#5-kuberenetes-applications)
- [6. Build Container Apllication from Source Code](#6-build-container-apllication-from-source-code)
- [7. Explore CNCF Landscape](#7-explore-cncf-landscape)
- [8. Entend Kubernetes Platform Capabilites](#8-entend-kubernetes-platform-capabilites)
  - [8.1. BareMetal Load-balancer - MetalLB](#81-baremetal-load-balancer---metallb)
  - [8.2. Ingress](#82-ingress)
  - [8.3. Kubernetes Gateway](#83-kubernetes-gateway)
  - [8.4. Service Mesh](#84-service-mesh)
- [9. Observability](#9-observability)
  - [9.1. Logging](#91-logging)
  - [9.2. Monitoring](#92-monitoring)
  - [9.3. Tracing](#93-tracing)
  - [9.4. Telemetry](#94-telemetry)
- [10. Example Use Case](#10-example-use-case)
  - [10.1. GitOps](#101-gitops)
- [11. CNCF Certification](#11-cncf-certification)
- [12. References](#12-references)


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



# 6. Build Container Apllication from Source Code

- [Build a simple application](./docs/build-container-application/README.md)




# 7. Explore CNCF Landscape

Ref: 
- https://landscape.cncf.io/



# 8. Entend Kubernetes Platform Capabilites

## 8.1. BareMetal Load-balancer - MetalLB

Ref: 
- https://metallb.universe.tf/

## 8.2. Ingress

Ref:
- https://kubernetes.github.io/ingress-nginx/
- https://docs.nginx.com/nginx-ingress-controller/ 
- https://medium.com/groupon-eng/loadbalancer-services-using-kubernetes-in-docker-kind-694b4207575d


## 8.3. Kubernetes Gateway

Ref:
- https://gateway-api.sigs.k8s.io/


## 8.4. Service Mesh
Ref:
- https://istio.io/
- https://linkerd.io/





# 9. Observability

## 9.1. Logging
- [Install Elastic Cloud on Kubernetes](./installation/elastic-cloud/elastic-cloud-kubernetes-installation.md)
- [Install Fluent-bit](./installation/fluent-bit/fluent-bit-installation.md)

## 9.2. Monitoring
- [Prometheus Operator Deployment](./installation/prometheus/prometheus-install.md)


## 9.3. Tracing

Ref:
- https://www.jaegertracing.io/


## 9.4. Telemetry

Ref:
- https://opentelemetry.io/


# 10. Example Use Case

## 10.1. GitOps


# 11. CNCF Certification

- Kubernetes and Cloud Native Associate (KCNA)
- Kubernetes and Cloud Security Associate (KCSA)
- Certified Kubernetes Administrator (CKA)
- Certified Kubernetes Application Developer (CKAD)
- Certified Kubernetes Security Specialist (CKS)

Ref:
- https://www.cncf.io/training/certification/




# 12. References
- https://docs.docker.com/get-docker/
- https://docs.docker.com/desktop/install/windows-install/
- https://kind.sigs.k8s.io/docs/user/using-wsl2/
- https://landscape.cncf.io/
- https://www.cncf.io/training/certification/