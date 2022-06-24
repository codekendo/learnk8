# CHP1

1.1 Understanding k8s

*API* used to define your applications

*Cluster* which runs your applications

A cluster is a set of individual servers that have been configured with a container runtime like Docker.
k8 container orchestrator.

A cluster is a single logical unit composed of many server nodes. Some nodes run the k8 api whereas other run application workloads in containers.

Each node has a container runtime installed.

Applications are defined in YAML files and deployed by sending the yaml to the cluster.
You manage the k8 applications remotely using the CLI that talks to the k8 API.

The cluster has a distrubuted database you can use to store both config files for your applications and secrets 

YAML are applications manifests

k8 run containers but it wraps them in other objects to support scale rolling updates and complex deployment patterns such as Pods and ReplicaSets and Deployments

External resources can be maanged by k8s and provided to containers.

Configuration is handled with ConfigMaps and Secrets. 
Storage is handled with volumes.



1.3.2
OSX Docker Desktop
Enable k8 in docker desktop preferences.

reset k8 Cluster

---

1.3.4

# macOS:
        brew install kubernetes-cli

1.3.7

alias k='kubectl'

k get nodes


# run a Pod with a single container; the restart flag tells Kubernetes
# to create just the Pod and no other resources:
kubectl run hello-kiamol --image=kiamol/ch02-hello-kiamol 



# wait for the Pod to be ready:
kubectl wait --for=condition=Ready pod hello-kiamol


# list all the Pods in the cluster: kubectl get pods
# show detailed information about the Pod: 
kubectl describe pod hello-kiamol




