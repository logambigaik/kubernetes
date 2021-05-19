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


![Uploading image.png…]()



````

POD
Create an NGINX Pod

kubectl run nginx --image=nginx



Generate POD Manifest YAML file (-o yaml). Don't create it(--dry-run)

kubectl run nginx --image=nginx  --dry-run=client -o yaml



Deployment


Create a deployment

kubectl create deployment --image=nginx nginx



Generate Deployment YAML file (-o yaml). Don't create it(--dry-run)

kubectl create deployment --image=nginx nginx --dry-run -o yaml



Generate Deployment with 4 Replicas

kubectl create deployment nginx --image=nginx --replicas=4



You can also scale a deployment using the kubectl scale command.

kubectl scale deployment nginx --replicas=4



Another way to do this is to save the YAML definition to a file.

kubectl create deployment nginx --image=nginx--dry-run=client -o yaml > nginx-deployment.yaml



You can then update the YAML file with the replicas or any other field before creating the deployment.



Service
Create a Service named redis-service of type ClusterIP to expose pod redis on port 6379

kubectl expose pod redis --port=6379 --name redis-service --dry-run=client -o yaml

(This will automatically use the pod's labels as selectors)

Or

kubectl create service clusterip redis --tcp=6379:6379 --dry-run=client -o yaml  (This will not use the pods labels as selectors, instead it will assume selectors as app=redis. You cannot pass in selectors as an option. So it does not work very well if your pod has a different label set. So generate the file and modify the selectors before creating the service)



Create a Service named nginx of type NodePort to expose pod nginx's port 80 on port 30080 on the nodes:

kubectl expose pod nginx --port=80 --name nginx-service --type=NodePort --dry-run=client -o yaml

(This will automatically use the pod's labels as selectors, but you cannot specify the node port. You have to generate a definition file and then add the node port in manually before creating the service with the pod.)

Or

kubectl create service nodeport nginx --tcp=80:80 --node-port=30080 --dry-run=client -o yaml

(This will not use the pods labels as selectors)

Both the above commands have their own challenges. While one of it cannot accept a selector the other cannot accept a node port. I would recommend going with the `kubectl expose` command. If you need to specify a node port, generate a definition file using the same command and manually input the nodeport before creating the service.



Reference:

https://kubernetes.io/docs/reference/kubectl/conventions/

```
