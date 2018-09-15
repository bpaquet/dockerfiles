# dockerfiles

Repo to store some useful dockerfiles.

## Kubernetes-snapshot-controller

    docker pull quay.io/bpaquet/kubernetes-snapshot-controller
    
Built from https://github.com/kubernetes-incubator/external-storage/tree/master/snapshot

Contains two binaries
* /snapshot-controller
* /snapshot-pv-provisioner

Kubernetes config can be found [here](https://blog.jetstack.io/blog/volume-snapshotting/). 
