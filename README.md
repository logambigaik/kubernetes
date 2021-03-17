# kubernetes

https://www.katacoda.com/courses/kubernetes/launch-single-node-cluster
https://training.linuxfoundation.org/resources/tutorials/set-up-a-ci-cd-pipeline-with-kubernetes-part-1-overview/

      >>  Kubernetes is an open-source system that handles the work of scheduling containers onto a compute cluster and manages the workloads to ensure they run as the user intends.
      >>  Kubernetes is an open source container Management tool which automates container deployment, container (de) scaling and container load balancing.
      >>  it works in all cloud vendors: Public,Hybrid & on-premises

Containers do not waste or block host resources unlike virtual machines. Containers have isolated libraries and binaries specific to the application they are running.


![image](https://user-images.githubusercontent.com/54719289/111199230-50bd6c00-85b8-11eb-8670-b08647989c82.png)

![image](https://user-images.githubusercontent.com/54719289/111200931-28cf0800-85ba-11eb-9a8c-a22b6fc817c9.png)

# Features of Kubernetes:

![image](https://user-images.githubusercontent.com/54719289/111201272-83686400-85ba-11eb-98c3-83d05de2b84e.png)

* Kubernets is not a docker
*           Docker      -->   Containerization platform
*           Kubernetes  -->   Conatiner manageable platform
*           Docker swarm also doing the same container manageable platform but auto scaling ,load balancing concept are missing . Manual intervention are required.
*           Kubernetes is not for simplle application architecture and preferrably for complex application

* Kubernetes is actually for,

![image](https://user-images.githubusercontent.com/54719289/111203189-97ad6080-85bc-11eb-971e-e7e9ee18ea15.png)

* Kubernetes Vs Docker Swarm:

![image](https://user-images.githubusercontent.com/54719289/111203704-3c2fa280-85bd-11eb-89f4-b869245ceb4b.png)


# POd is collection of COntainer:

![image](https://user-images.githubusercontent.com/54719289/111211222-1064ea80-85c6-11eb-8fff-25acfe34c87c.png)


![image](https://user-images.githubusercontent.com/54719289/111211375-3be7d500-85c6-11eb-98dd-34f591a504f4.png)

![image](https://user-images.githubusercontent.com/54719289/111211479-5b7efd80-85c6-11eb-8562-7cb46354d98c.png)

![image](https://user-images.githubusercontent.com/54719289/111211560-73ef1800-85c6-11eb-8f69-20266f149888.png)


# Difference between Docker swarm and kubernetes:

![image](https://user-images.githubusercontent.com/54719289/111358918-cbeb5480-8682-11eb-86dd-de5483d1adf7.png)

# Microservices:

![image](https://user-images.githubusercontent.com/54719289/111360230-65ffcc80-8684-11eb-8c4b-25521a5fa178.png)

If any issue in any one of microservices then deployment is required only for that service after fixing the issue not all the services.


![image](https://user-images.githubusercontent.com/54719289/111361673-d9eea480-8685-11eb-94a0-e1e853414f06.png)

# Scaling:

![image](https://user-images.githubusercontent.com/54719289/111526212-5d77c680-8756-11eb-9ecf-8f2cee587b3e.png)

* Scaling:
      
            >>    Horizontal Pod Autoscale  - wil increase the no of pods
                  The Horizontal Pod Autoscaler automatically scales the number of Pods in a replication controller, deployment, replica set or stateful set based on observed CPU utilization
            >>    Vertical Pod Autoscale  - will increase the cpu memory of pod
            >>    Cluster Autoscale       - will increase the kubernetes nodes


# Container Setup:

![image](https://user-images.githubusercontent.com/54719289/111528291-e0018580-8758-11eb-9249-2e5e30b7ee6d.png)

Kubernetes: Kubernetes utilizes its own YAML, API, and client definitions and each of these differ from that of standard docker equivalents. That is to say, you cannot utilize Docker Compose nor Docker CLI to define containers. While switching platforms, YAML definitions and commands need to be rewritten.

Docker Swarm: The Docker Swarm API doesn’t entirely encompass all of Docker’s commands but offers much of the familiar functionality from Docker. It supports most of the tools that run with Docker. Nevertheless, if Docker API is deficient of a particular operation, there doesn’t exist an easy way around it around swarm.

# Load Balance:

Kubernetes: Pods are exposed via service, which can be utilized as a load balancer within the cluster. Generally, an ingress is utilized for load balancing.

Docker Swarm: Swarm mode consists of a DNS element that can be utilized for distributing incoming requests to a service name. Services can be assigned automatically or can run on ports specified by the user.

# Networking:

![image](https://user-images.githubusercontent.com/54719289/111539574-ee09d300-8765-11eb-9c49-5dc66a64da8b.png)

# Availability:
![image](https://user-images.githubusercontent.com/54719289/111539702-15f93680-8766-11eb-8232-23de7f4c7a6d.png)


# Logging and Monitoring (K8s Vs swarm):

![image](https://user-images.githubusercontent.com/54719289/111540546-2e1d8580-8767-11eb-8edc-3a65147da114.png)


# GUI:

![image](https://user-images.githubusercontent.com/54719289/111540723-6755f580-8767-11eb-8f18-bcc125f31250.png)


# Which is best swarm or k8s:

![image](https://user-images.githubusercontent.com/54719289/111541316-36c28b80-8768-11eb-8d9e-46ee737351d6.png)


