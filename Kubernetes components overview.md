******************************************
**** Kubernetes Architecture Overview ****
******************************************
![IMG](https://github.com/satya3318/kubernetes/blob/main/Screenshot%202026-05-28%20143729.png)

What is Kubernets:
Kubernetes, often abbreviated as K8s, is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications. It provides a framework to efficiently manage the complexities of deploying and running applications in containers across a cluster of machines.

Kubernetes mainly has two parts:
1. Control Plane (Master Node)
2. Worker Nodes

— CONTROL PLANE:
The master control plane is the central management unit of a Kubernetes cluster. It oversees the entire cluster’s operation and coordination, making high-level decisions about how applications should run and ensuring that the actual state of the cluster matches the desired state.

1. API Server:The API Server acts as the entry point for interactions with the Kubernetes cluster. It exposes the Kubernetes API, which allows users, administrators, and other components to communicate with the cluster.

2. etcd:etcd is a distributed key-value store that serves as Kubernetes’ backing store for all cluster data. It holds the configuration data and the state of the entire cluster. This includes information about Pods, Services, replication settings, and more.

3. Controller Manager:The Controller Manager is responsible for monitoring the state of various objects in the cluster and taking corrective actions to ensure the desired state is maintained. It includes several built-in controllers, such as the Replication Controller, Deployment Controller, and StatefulSet Controller.

4. Scheduler:The Scheduler is responsible for placing Pods onto suitable worker nodes. It takes into account factors like resource availability, constraints, and optimization goals.

