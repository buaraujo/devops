# Redis on Kubernetes

## StatefulSet: Redis Server (3 instances)

```
kubectl apply -n redis -f ./redis-server-config.yml
kubectl apply -n redis -f ./redis-server-service.yml
kubectl apply -n redis -f ./redis-server-statefulset.yml

kubectl -n redis get pods
kubectl -n redis get pv
```

## StatefulSet: Redis Sentinel (3 instances)

```
kubectl apply -n redis -f ./redis-sentinel-service.yml
kubectl apply -n redis -f ./redis-sentinel-statefulset.yml

kubectl -n redis get pods
kubectl -n redis get pv
```