# jenkins
Jenkins on K8s (Digital Ocean Managed) 

## Setup
1. Create a namespace called jenkins.
2. Apply the yaml files within the namespace.
3. Log into jenkins (find admin password in pod log), install default plugins.
4. Enable proxying in settings to get rid of annoying crumb error.
5. Install kubernetes (and Blue Ocean) plugins.
6. Set up a kubernetes cloud, point pod template image to custom jenkins agent image.
7. Set up docker daemon deployment and service in the kubernetes cluster.
8. Make sure to pass the DOCKER\_HOST env variable to the jenkins agent with the address of the docker daemon service.

9. (Optional) set up local registry

## To Do
Get kubectl working within the Jenkins agent. 
1. Create a kubernetes secret from the kubeconfig.yaml file.
2. Pass this through to the jenkins agent.
