# High-Availability Wordpress hosted on Kubernetes

## Architecture
1. NFS Server as StatefulSet with PersistentVolume from an existing GCE Persistent Disk
2. Multiple replicas of Wordpress with PersistentVolume from NFS using ReadWriteMany access mode

## Prerequisites
1. Kustomize v3.8.4
2. Google Kubernetes Engine v1.16.13-gke.401

## How-To
```bash
$ git clone https://github.com/ardikabs/ha-k8s-wordpress
$ kustomize build ha-k8s-wordpress | kubectl apply -n wordpress -f -
```