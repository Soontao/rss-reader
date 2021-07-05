# RSS Reader

Minimal RSS Reader, k8s readyd

## Table of Contents

- [RSS Reader](#rss-reader)
  - [Table of Contents](#table-of-contents)
  - [docker-compose](#docker-compose)
  - [k8s native artifacts](#k8s-native-artifacts)
  - [helm artifacts](#helm-artifacts)
  - [DNS Utils](#dns-utils)

## docker-compose

deploy

```bash
docker-compose up -d
```

un-deploy

```bash
docker-compose down
```

## k8s native artifacts

build

```bash
kompose convert --out ./kube-artifacts
```

deploy

```bash
kubectl apply -f ./kube-artifacts
```

undeploy

```bash
kubectl delete -f ./kube-artifacts
```

## helm artifacts

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