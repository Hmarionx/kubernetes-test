# kubernetes

Add certificates:


```sh
mkvenv certbot
venv certbot
pip install certbot-plugin-gandi
sudo /home/nicocti/.virtualenvs/certbot/bin/certbot certonly --authenticator dns-gandi --dns-gandi-credentials ./gandi.ini -d lan.repe.re -d \*.lan.repe.re --server https://acme-v02.api.letsencrypt.org/directory
kubectl create -n ingress-nginx secret tls cert-lan-repe-re --key ./tls.key --cert ./tls.crt
kubectl apply -f nginx/
kubectl apply -f portainer/
```

```sh
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm show values prometheus-community/prometheus
helm install --dry-run --debug --namespace monitoring --create-namespace 13.6.0 prometheus-community/prometheus
```
