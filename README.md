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
make deploy
```

### Deploy app

```
kubectl create -f config/samples/webapp_v1_redis.yaml
kubectl create -f config/samples/webapp_v1_mywatchlist.yaml
```

### Forward port

```
kubectl get mywatchlist
kubectl port-forward svc/mywatchlist-sample 7000:8080
```
