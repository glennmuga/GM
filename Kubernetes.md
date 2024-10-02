## Kubernetes 

Kubernetes is a powerful open-source platform for automating deployment, scaling, and operations of application containers across clusters of hosts.

It provides a container-centric infrastructure that is efficient, making it a leading choice for managing complex applications

## What is Kubernetes?
Kubernetes is an open-source platform designed to automate deploying, scaling, and operating application containers. 

## Kubernetes Architecture 
![image](https://github.com/user-attachments/assets/34d7ea26-2fa0-4976-a355-e16ab819c8d0)

Kubernetes is an open-source container deployment and administration platform. It offers container orchestration, container runtime, container-centric infrastructure orchestration, balance of load, self-healing mechanisms, and service discovery. A Kubernetes cluster has several control planes and one or more worker nodes.

## Explain the concept of Container Orchestration.
Container orchestration is a tool that developers may use anywhere there are containers to automate the life cycle management of the containers. 

It provides a automatic deployment, scaling, and management of containerized applications so that the developers do not have any worry about that the underlying infrastructure.

## What is a Pod in Kubernetes?
A cluster of one or more Linux containers makes up a Kubernetes pod, the smallest unit of a Kubernetes application. 

From the more common scenario of a single container to an advanced use case with numerous tightly coupled containers within a pod, this basic structure allows for an array of designs.

kubectl get pods -n <namespace-name>

## How does Kubernetes handle container scaling?
To automatically scale the workload to match demand, a Horizontal Pod Autoscaling in Kubernetes updates a workload resource (such a deployment or stateful set). 

Horizontal scaling indicates that more pods are added in response to an increase in load.


apiVersion: autoscaling/v2beta2

kind: HorizontalPodAutoscaler

metadata:

name: my-hpa

spec:

scaleTargetRef:

apiVersion: apps/v1

kind: Deployment # or StatefulSet, or ReplicaSet, depending on your workload

name: my-deployment

minReplicas: 3

maxReplicas: 5

metrics:

– type: Resource

resource:

name: cpu

target:

type: Utilization

averageUtilization: 65


## What is Kubelet?
Kubelet is an important component of Kubernetes that manages containers within pods on a node. 

It registers the node with the control plane and provides resource information. Kubelet keeps an eye on container health and responds to problems—lik isnces of pods that contain a containerized application. 

## What is a Service in Kubernetes?
The idea of the Service is to group a set of Pod endpoints into a single resource. We can configure various ways to access the grouping. By default, we can get a stable cluster IP address that the clients inside the cluster can use to contact Pods in Service.

apiVersion: v1

kind: Service

metadata:

name: my-service

spec:

selector:

Tomcat: deploymentapp

ports:

– protocol: TCP

port: 80

targetPort: 8080

## Describe the role of a Master node in Kubernetes.
Kubernetes master node components can be run within Kubernetes itself, as a set of containers within the dedicated pod. 

The master node is responsible for cluster management and for providing the API that is used to configure and manage resources within the Kubernetes cluster.

## What is the role of the kube-proxy in Kubernetes and how does it facilitate communication between Pods?
The networking part of Kubernetes that enables communication between pods & services is called Kube-proxy, and it may be installed on any cluster node.

Its major function is to maintain network rules for service-to-pod mapping, which provides communication to and from Kubernetes clusters.

## Explain the concept of Ingress in Kubernetes.
In the following section, we will go across what Kubernetes Ingress is, what an Ingress controller is, how it fixes routing difficulties, and how to implement it step-by-step. 

Ingress is a Kubernetes API object that is used to expose HTTP and HTTPS routes from outside the cluster to services inside the cluster. It provides a single entry point into a cluster, it allows more straightforward management applications and troubleshooting routing issues.

![image](https://github.com/user-attachments/assets/87f03e67-c9f7-4e76-a8cf-8d413bbed421)

##  Describe the role of etcd in Kubernetes.
Etcd is the cluster brain that maintains records of all cluster information, which includes the desired state, the current state, resource configurations, and runtime data.

It is the cluster brain that informs other processes that including the Scheduler about changes in the cluster state and availability of resources.

## How do rolling updates work in a Deployment?
The rolling update deployment strategy, additionally referred to as a rolling deployment, makes sure of zero downtime by methodically replacing out of date Pods with updated ones, facilitating a smooth transition during Deployment updates.

A rolling deployment is a strategic approach that gradually substitutes older versions of an application with newer ones through an overall replacement of the underlying infrastructure.

## What is a Namespace in Kubernetes?
Namespaces permit Kubernetes clusters to be organized into virtual sub-clusters, which is useful in situations where a cluster is utilized by several teams or projects. 

Namespaces allow a cluster to be structured in any number of ways, with each namespace providing logical segregation from the others while maintaining the ability to speak across namespaces.

## Explain the use of Labels and Selectors in Kubernetes.
Labels and Selectors are essential sections in Kubernetes configuration files for deployments and services due to how they link Kubernetes services to pods.

Labels are key-value pairs that identify pods distinctly; the deployment assigns these labels and uses them as a starting point for the pod prior to its creation, and the Selector matches these labels. 

Labels and selectors combine to create connections between deployments, pods, and services in Kubernetes.

## Replicaset

On any node, ReplicaSet will make sure that the number of operating pods in the Kubernetes cluster match the number of pods that is planned.

## What is a Kubernetes cluster?

A Kubernetes cluster is a set of nodes that run containerized applications managed by the Kubernetes control plane.

## What is a node in Kubernetes?

A node is a worker machine in Kubernetes that runs containerized applications.

## What is a Kubernetes replica set?

A Kubernetes replica set ensures that a specified number of replicas of a pod are running at any given time.

## What is kubectl?

kubectl is the command-line tool used to interact with a Kubernetes cluster.

## What is Kubernetes kubectl logs?

Kubernetes kubectl logs is the command to retrieve the logs generated by a specific pod.

## What is Kubernetes kubectl describe?

Kubernetes kubectl describe is the command to get detailed information about a Kubernetes object, such as a pod, replication controller, or service.
Kubernetes Cluster Administration

## Kubernetes commands :
![image](https://github.com/user-attachments/assets/07acb2bc-524c-4459-9d81-18768ffed211)

![image](https://github.com/user-attachments/assets/aa623483-b220-4226-96d0-f0abdb901745)

kubectl apply -f <filename.yaml> 

Getting  Nodes: The number of available nodes in the cluster will be displayed by “Kubectl get nodes”. 

Getting Pods: “Kubectl get pod” can be used to find out how many pods are scheduled in the cluster.

Getting Services: “Kubectl get service” can be used to list the services that have been created in the cluster.

kubectl delete <resource_type> <resource_name> | --all

 kubectl apply -f [file-name]

 kubectl delete -f [file-name]

 Viewing Logs of a Pod: The command shows the logs of the pod mentioned once the pod started.
$ kubectl logs [pod-name]

Get info about a Resource: The command gives details about the nginx deployment
$ kubectl describe <resource_type> [resource-name]

With the help of the “kubectl cp” command, we can copy files from host to container and vice versa.

The basic syntax of “kubectl  cp”

kubectl cp <host path pod name:container path> 

![image](https://github.com/user-attachments/assets/b99b8513-66ad-48b2-8a1c-ae6c700b3d39)

## Kubernetes master node 
Kubernetes Master Node Components Important Terminologies
API Server
Scheduler
Controller-Manager
etcd

API Server

Kube API Server interacts with API, its a frontend of the kubernetes control plane. Communication center for developers and other kubernetes components.Receiving queries from multiple clients, including the kubectl command-line tool, the API server serves as the front-end interface for the Kubernetes control plane, coordinating cluster-wide operations.


Scheduler

The scheduler watches the pods and assigns the pods to run on specific hosts. A new pod does not have a specific node assigned when it is formed, whether by a user, a deployment controller, or a replication controller. The scheduler chooses a suitable node for the pod to run on after assessing the resource needs of the pod, such as CPU and memory usage, as well as any restrictions or affinity/anti-affinity rules supplied.


Controller-Manager

The controller manager runs the controllers in the background which run different tasks in the kubernetes cluster. Performs cluster-level functions(Replication, Tracking worker nodes, Handling failures).


etcd

etcd is a simple distributed key-value store. kubernetes uses etcd as its database to store all cluster data. Some of the data stored in etcd is job scheduling information, pods, state information and etc.

## worker node 
Kubernetes Worker Node Components Important Terminologies
Worker nodes are the node where the application actually runs in a kubernetes cluster, it is also known as a minion. These worker nodes are controlled by the master node using Kublet processes.

kubelet
kube-Proxy
Container runtime

Kubelet

The main node agent, known as Kubelet, operates on each node and reads the container manifests to make sure that the containers are active and in good condition. It ensures that pods of containers are operating. Containers that weren’t made by Kubernetes are not managed by the kubelet.


Kube-Proxy

By managing network rules on the host and managing connections, kube-proxy supports the kubernetes service abstraction. On nodes, Kube-proxy keeps track of network rules. Network connectivity to your pod is permitted by these network rules from both inside and outside of your cluster. Having a network proxy and load balancer for the service on a single worker node is beneficial to us.


Container Runtime

To process commands from the master server to run containers, each node needs a container runtime, such as Docker, containerd, or another container runtime.
