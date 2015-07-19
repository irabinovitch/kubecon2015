# Nginx Summit Demo


```
kubectl run hello-v1 \
  --labels="version=1.0.0,app=hello,track=stable" \
  --image=quay.io/kelseyhightower/hello:1.0.0
```

```
kubectl create -f hello-svc.yaml
```

```
kubectl scale rc hello-v1 --replicas=100
```

```
kubectl run hello-canary \
  --labels="version=2.0.0,app=hello,track=canary" \
  --replicas=11 \
  --image=quay.io/kelseyhightower/hello:2.0.0
```

```
kubectl create -f hello-canary-svc.yaml
```

```
kubectl create -f hello-v1-svc.yaml
```

```
kubectl create -f hello-v2-svc.yaml
```
