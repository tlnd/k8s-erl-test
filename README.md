# Erlang node communication in kubernetes cluster

This repository holds some deployments to experiment with Erlang node
communication in kubernetes clusters.


## Central registry

There is a pod behind a k8s service, that acts as central registration point.
All worker nodes need to connect to that node in order to become part of the
node cluster.


## Stateful Set

The StatefulSet creates named pods that can be used to connect to each other,
by using the headless service for the StatefulSet, e.g.
`net_kernel:connect('sts@erl-worker-sts-1.erl-worker-sts')`
