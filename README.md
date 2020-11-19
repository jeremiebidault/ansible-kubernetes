# kubernetes deployment

OS : centos

container runtime : docker

container network interface : weave

high availability : keepalived && haproxy

# roles

## bootstrap

install base packages

## candidate

order first initialized kubernetes master then clean nodes under a group hosts called "candidate"

## certificates

generates certificates for etcd cluster

## docker

install docker packages and setup the system

## etcd

install etcd packages and setup the cluster

## haproxy

install haproxy packages and setup the cluster

## init

init first kube-master, generates certificates and join commands for other kube-master && kube-node

## keepalived

install keepalived packages and setup the cluster

## kubernetes

install kubernetes packages and setup the system

## master

add kube-master to cluster

## node

add kube-node to cluster

## remove

clean kubernetes, etcd, haproxy and keepalived config

# ongoing

- make remove role
- replace certs files by facts
- untaint hosts that are in kube-master && kube-node
- many more...