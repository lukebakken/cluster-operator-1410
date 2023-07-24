# cluster-operator-1410

https://github.com/rabbitmq/cluster-operator/discussions/1410

## Reproduction attempt

```
kubectl apply --filename ./new-rabbitmq.yaml

# wait for node to be running

kubectl apply --filename ./rabbitmq.yaml

# wait for cluster to be running

kubectl delete --filename ./rabbitmq.yaml

```

Result after running the above commands:

```
lbakken@shostakovich ~/development/lukebakken/cluster-operator-1410 (main *=)
$ kubectl get pod
NAME                    READY   STATUS    RESTARTS   AGE
new-rabbitmq-server-0   1/1     Running   0          8m41s
```
