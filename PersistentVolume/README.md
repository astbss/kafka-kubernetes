## First create the local folders used by PersistentVolume
```
- mkdir -p /var/kafka/broker ; mkdir -p mkdir -p /var/kafka/pzoo ; chmod -R 777 /var/kafka

```



## Apply PersistentVolume Settings
**You need to edit this files and add your node name to the end**
```
- kubectl apply -f ./PersistentVolume/PersistentVolume-broker.yml
- kubectl apply -f ./PersistentVolume/PersistentVolume-pzoo.yml

```
## Sources and Documentation
```
- https://kubernetes.io/docs/concepts/storage/volumes/#local
- https://github.com/Yolean/kubernetes-kafka/tree/master/configure
```
