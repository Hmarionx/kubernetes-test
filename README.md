# kubernetes

Add certificates:

```sh
kubectl create -n ingress-nginx secret tls cert-lan-repe-re --key ./tls.key --cert ./tls.crt
```
