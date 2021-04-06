# kubernetes

Add certificates:


```sh
kubectl create -n ingress-nginx secret tls cert-lan-repe-re --key ./tls.key --cert ./tls.crt
kubectl apply -f nginx/
kubectl apply -f portainer/
```

```sh
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm show values prometheus-community/prometheus
helm install --dry-run --debug --namespace monitoring --create-namespace 13.6.0 prometheus-community/prometheus
```
