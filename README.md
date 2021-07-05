# RSS Reader

Minimal RSS Reader

## K8s native artifacts

build

```bash
kompose convert --out ./kube-artifacts
```

deploy

```bash
kubectl apply -f ./kube-artifacts
```

## Helm artifacts

```bash
kompose convert -c --out ./helm-charts
```

## DNS Utils

```bash
# apply deployment
kubectl apply -f https://k8s.io/examples/admin/dns/dnsutils.yaml
# check pods is ready
kubectl get pods dnsutils
# check dns with name 
kubectl exec -i -t dnsutils -- nslookup pg 
```