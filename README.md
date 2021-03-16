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
