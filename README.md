# My watchlist

### Build the controller

```
make docker-build
```

### Deploy CRD

```
make install
```

### Deploy operator manager

```
make deploy IMG=micabe/controller-watchlist
```

### Deploy app

```
kubectl create -f operator/config/samples/webapp_v1_redis.yaml
kubectl create -f operator/config/samples/webapp_v1_mywatchlist.yaml
```

### Forward port

```
kubectl get mywatchlist

kubectl port-forward svc/mywatchlist-sample 7000:8080
```

### cleanup

```
kubectl delete -f operator/config/crd/bases/
kubectl delete -f operator/config/samples/webapp_v1_redis.yaml
kubectl delete -f operator/config/samples/webapp_v1_mywatchlist.yaml
```
