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