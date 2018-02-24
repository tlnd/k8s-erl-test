# Erlang node communication in kubernetes cluster

This repository holds some deployments to experiment with Erlang node
communication in kubernetes clusters.


## Central registry

There is a pod behind a k8s service, that acts as central registration point.
All worker nodes need to connect to that node in order to become part of the
node cluster.
