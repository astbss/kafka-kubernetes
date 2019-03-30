
# Kafka on Kubernetes

Transparent Kafka setup that you can grow with.
Good for both experiments and production.

How to use:
 * Run a Kubernetes cluster, [minikube](https://github.com/kubernetes/minikube) or real.
 * Quickstart: use the `kubectl apply`s below.

No readable readme can properly introduce both [Kafka](http://kafka.apache.org/) and [Kubernets](https://kubernetes.io/),
but we think the combination of the two is a great backbone for microservices.

## What you get

Keep an eye on `kubectl --namespace kafka get pods -w`.

The goal is to provide [Bootstrap servers](http://kafka.apache.org/documentation/#producerconfigs): `kafka-0.broker.kafka.svc.cluster.local:9092,kafka-1.broker.kafka.svc.cluster.local:9092,kafka-2.broker.kafka.svc.cluster.local:9092`
`

Zookeeper at `zookeeper.kafka.svc.cluster.local:2181`.

## Start Zookeeper

The [Kafka book](https://www.confluent.io/resources/kafka-definitive-guide-preview-edition/) recommends that Kafka has its own Zookeeper cluster with at least 5 instances.

```
kubectl apply -f ./zookeeper/
```

## Start Kafka

```
kubectl apply -f ./
```

To get consistent service DNS names kafka-N.broker.kafka (.svc.cluster.local), run everything in a namespace.<br>
Use a headless service to create DNS records (20dns.yml)

That's it. Just add business value :wink:.

## RBAC

For clusters that enfoce [RBAC](https://kubernetes.io/docs/admin/authorization/rbac/) there's a minimal set of policies in
```
kubectl apply -f rbac-namespace-default/
```

# Sources and inspiration
- https://github.com/Yolean/kubernetes-kafka
- Special thanks to Yolean, Solsson and many others for their amusing work
- https://hub.docker.com/r/solsson/kafka/
- https://kubernetes.io/docs/concepts/storage/volumes/#local
- http://wurstmeister.github.io/kafka-docker/





- 
- 
- 
- 

