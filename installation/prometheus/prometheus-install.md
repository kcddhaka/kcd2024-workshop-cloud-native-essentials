# Install Prometheus Operator Deployment

Helm chart of prometheus-operator is maintain in the [prometheus-community repo](https://github.com/prometheus-community/helm-charts) with name [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack).

Components included in this package:
- The Prometheus Operator
- Highly available Prometheus
- Highly available Alertmanager
- Prometheus node-exporter
- Prometheus Adapter for Kubernetes Metrics APIs
- kube-state-metrics
- Grafana


```bash
# add helm repo
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
```

Check default supported value by the kube-prometheus-stack:
```bash
helm show values prometheus-community/kube-prometheus-stack > default-kube-prometheus-stack-values.yaml
more default-kube-prometheus-stack-values.yaml
```

Install:
```bash
# install without any custom value
helm install kube-prometheus-stack \
  --create-namespace \
  --namespace kube-prometheus-stack \
  prometheus-community/kube-prometheus-stack -f custom-values-stack.yaml
```


# GUI Access uing Port-forwarding

# Create Ingress for Prometheus GUI


# References
- 