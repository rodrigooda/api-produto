**Product Kubernetes sample Application** 
Kubernetes/GKE
This application works on any Kubernetes cluster, as well as Digital Ocean
Kubernetes Engine..

## Quickstart

1. **[Create a DigitalOcean Kubernetes](https://docs.digitalocean.com/products/kubernetes/how-to/create-clusters/)** 
```
Download the configuration file from the kubernets control panel (Quick Start Guide)
```

2. **Clone this repository.**

```
git clone https://github.com/rodrigooda/api-produto.git
cd api-produto
```

3. **Deploy the sample app to the cluster.**

```
kubectl apply -f ./k8s -R
```

5. **Check if the structure is created.**

```
kubectl get all
```

6. **[Install Helm](https://helm.sh/docs/intro/install/)**

7. **Add prometheus to kubernetes cluster.**
```
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo add kube-state-metrics https://kubernetes.github.io/kube-state-metrics
helm repo update
helm install prometheus prometheus-community/prometheus --values ./Prometheus/values.yaml
```
7. **Add grafana to kubernetes cluster.**
```
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
helm install grafana grafana/grafana --values ./Grafana/values.yaml
```