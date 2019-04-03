## You need to first create the local folders used by PersistentVolume
```
- mkdir -p /var/kafka/broker ; mkdir -p mkdir -p /var/kafka/pzoo ; chmod -R 777 /var/kafka

```



## Edit and Start PersistentVolume
```
- https://kubernetes.io/docs/concepts/storage/volumes/#local
- https://github.com/Yolean/kubernetes-kafka/tree/master/configure
```
```
- kubectl apply -f ./PersistentVolume/PersistentVolume-broker.yml
- kubectl apply -f ./PersistentVolume/PersistentVolume-pzoo.yml

```
