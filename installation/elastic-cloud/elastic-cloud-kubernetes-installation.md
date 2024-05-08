# Install Elastic Cloud on Kubernetes(ECK)

ECK Components:
- Elasticsearch
- Kibana
- Elastic Agent
- Fleet Server
- Beats
- Logstash
- APM Server


Add helm repo:
```bash
helm repo add elastic https://helm.elastic.co
helm repo update
```


## Install ECK Operator
```bash
# Add the Elastic Helm Repository
helm repo add elastic https://helm.elastic.co && helm repo update

# Install the ECK Operator cluster-wide
helm install elastic-operator elastic/eck-operator -n elastic-system --create-namespace
```


## Install ECK Stack

```bash
# Add the Elastic Helm Repository
helm repo add elastic https://helm.elastic.co && helm repo update

# Install the ECK-Stack helm chart
# This will setup a 'quickstart' Elasticsearch and Kibana resource in the 'elastic-stack' namespace
helm install my-release elastic/eck-stack -n elastic-stack --create-namespace
```

Now change service config to get LB IP address: 
- extract password: k get secrets -n elastic-stack elasticsearch-es-elastic-user -o go-template='{{.data.elastic | base64decode}}'
- Find Kibana IP Address
- Find Elastic Search IP Address



# References
- https://www.elastic.co/guide/en/cloud-on-k8s/current/k8s-stack-helm-chart.html
- https://github.com/elastic/cloud-on-k8s/tree/main/deploy