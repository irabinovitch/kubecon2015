# Nginx Summit Demo

```
kubectl run hello \
  --labels="app=hello,track=stable" \
  --image=quay.io/kelseyhightower/hello:1.0.0
```

```
kubectl create -f hello-svc.yaml
```

```
kubectl scale rc hello --replicas=100
```

```
kubectl run hello-canary \
  --labels="app=hello,track=canary" \
  --replicas=11 \
  --image=quay.io/kelseyhightower/hello:2.0.0
```

```
kubectl create -f hello-stable-svc.yaml
```

```
kubectl create -f hello-canary-svc.yaml
```

```
kubectl rolling-update hello --update-period=3s --image=quay.io/kelseyhightower/hello:2.0.0
```
