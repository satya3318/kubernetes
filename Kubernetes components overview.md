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

1. API Server(kube-apiserver):The API Server acts as the entry point for interactions with the Kubernetes cluster. It exposes the Kubernetes API, which allows users, administrators, and other components to communicate with the cluster.

2. etcd:etcd is a distributed key-value store that serves as Kubernetes’ backing store for all cluster data. It holds the configuration data and the state of the entire cluster. This includes information about Pods, Services, replication settings, and more.

3. Controller Manager(kube-controller-manager):The Controller Manager is responsible for monitoring the state of various objects in the cluster and taking corrective actions to ensure the desired state is maintained. It includes several built-in controllers, such as the Replication Controller, Deployment Controller, and StatefulSet Controller.

4. Scheduler(kube-scheduler):The Scheduler is responsible for placing Pods onto suitable worker nodes. It takes into account factors like resource availability, constraints, and optimization goals.

— WORKER NODES:
Worker nodes, also known as worker machines or worker servers, are the heart of a Kubernetes cluster. They are responsible for running containers and executing the actual workloads of your applications.

1. Kubelet: The Kubelet is an agent that runs on each worker node and communicates with the master control plane. Its primary responsibility is to ensure that containers within Pods are running and healthy as per the desired state defined in the cluster’s configuration. The Kubelet works closely with the master control plane to start, stop, and manage containers based on Pod specifications.

2. Kube Proxy: Kube Proxy sets up routing and load balancing so that applications can seamlessly communicate with each other and external resources.

3. Container Runtime:A container runtime is the software responsible for running containers on the worker nodes.

4. Container Storage Interfaces (CSI):Worker nodes need to provide storage for persistent data. Kubernetes supports different storage solutions through Container Storage Interfaces (CSI). These interfaces allow different storage providers to integrate with Kubernetes and offer persistent storage volumes for applications.
