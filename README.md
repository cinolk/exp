**How to deploy the below docker image using kubernets **

https://hub.docker.com/r/paulbouwer/hello-kubernetes

Use a new seperate/newspace to isolate  projects and microservices from others.

Deployment section to create a pod using the hello-kuberetes image. 

A service is defined to expose the ports to the ourside word and mapped the port to the contaner port. 

HPA configured to automatically increasing or decreasing the number of Pods in response to the workload.

An ingress rule has been set in such a way that any calls in ingressip/DNS with base path "/" will be routed to hello-kubernetes service. 



To execute
$ kubectl apply -f hellokube.yaml

To see all the resouces 
$kubectl get all -n dev-app-ns

