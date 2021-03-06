# **Kubernetes Talk**
Let's talk about kubernetes
### **Table of Contents**
1. [Options of How We Can Deploy Our Application](https://github.com/ludesdeveloper/kubernetes-talk#options-of-how-we-can-deploy-our-application)
2. [Table Comparison Deployment Method](https://github.com/ludesdeveloper/kubernetes-talk#table-comparison-deployment-method)
3. [Where to Start](https://github.com/ludesdeveloper/kubernetes-talk#where-to-start)
4. [Learning Linux](https://github.com/ludesdeveloper/kubernetes-talk#learning-linux)
5. [What is Container](https://github.com/ludesdeveloper/kubernetes-talk#what-is-container)
6. [How to Get Your Hands Dirty with Container](https://github.com/ludesdeveloper/kubernetes-talk#how-to-get-your-hands-dirty-with-container)
7. [Pipeline](https://github.com/ludesdeveloper/kubernetes-talk#pipeline)
8. [Table Comparison Pipeline](https://github.com/ludesdeveloper/kubernetes-talk#table-comparison-pipeline)
9. [What is Kubernetes](https://github.com/ludesdeveloper/kubernetes-talk#what-is-kubernetes)
10. [Kubernetes Components](https://github.com/ludesdeveloper/kubernetes-talk#kubernetes-components)
11. [Kubernetes Objects](https://github.com/ludesdeveloper/kubernetes-talk#kubernetes-objects)
12. [Create Kubernetes Cluster](https://github.com/ludesdeveloper/kubernetes-talk#create-kubernetes-cluster)
13. [Interaction with Kubernetes Cluster](https://github.com/ludesdeveloper/kubernetes-talk#interaction-with-kubernetes-cluster)
### **Options of How We Can Deploy Our Application**
![Serverless Evolution](pic/serverless_evolution.png)
### **Table Comparison Deployment Method**
|   | Bare Metal | Virtual Machines | Containers | Functions |
| - | - | - | - | - |
| Learning curve | Hardest  | Hard  | Medium | Easy |
| Deployment difficulty | Hardest  | Hard  | Medium | Easy |
| Time to deploy | Slowest  | Medium  | Fast | Very Fast |
| How much do we need SysOps | 100 percent yes | Yes we need | If Dev understand container, answer is no | Not at all |
### **Where to Start**
```mermaid
flowchart LR
A[Linux] --> B[Container]
B --> C[Pipeline]
C --> D[Kubernetes]
```
### **Learning Linux**

<p align="center">
  <img width="695" height="494" src="pic/linux-thug-life.jpeg">
</p>

Everyone has different approach for learning, Me myself learning linux with installing linux on my computer, and make it my daily driver, it will
easier for me to push myself to live in linux terminal. But you also can install it in [WSL](https://docs.microsoft.com/en-us/windows/wsl/install), 
[VM](https://www.virtualbox.org/), or provision it in Cloud.

Why we need to "taste" linux first before we can continue to container? Most of command used in container is unix, linux based command, so it make sense
if try linux before we go to container
### **What is Container**
![Use containers to Build, Share and Run your applications](pic/container-what-is-container.png)
For detail you can read from [here](https://www.docker.com/resources/what-container), but IMHO, container is how you can package your application
with it's dependency so you can run it anywhere.
### **How to Get Your Hands Dirty with Container**
1. [Install Docker](https://docs.docker.com/get-docker/)
2. [Create Dockerfile](https://docs.docker.com/language/python/build-images/)
### **Pipeline**
![CI/CD](pic/CI-CD.png)
Something will missing if you try to learn kubernetes without try to understand about Pipeline, here is good [article](https://docs.gitlab.com/ee/ci/introduction/)
for that. IMHO, Pipeline is how we can automate process from your push your code, untill it release, operate, even put some security process inside it
### **Table Comparison Pipeline**
| | Code | Build | Test | Release | Deploy | Operate | Monitor | Security |
| - | - | - | - | - | - | - | - | - |
| Continuous Integration | X | X | X | - | - | - | - | - |
| Continuous Delivery | X | X | X | X | - | - | - | - |
| Continuous Deployment | X | X | X | X | X | - | - | - |
| DevOps | X | X | X | X | X | X | X | - |
| DevSecOps | X | X | X | X | X | X | X | X |
> Yeah, there is new kid on the block, GitOps, i'm too confuse too put it in table, check [argo cd](https://argo-cd.readthedocs.io/en/stable/)
one of GitOps tools/implementation out there
### **What is Kubernetes**
For TLDR, [check this out](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/).

I couldn't describe how much I love K8S (Kubernetes),
Some feature that i really love is self healing (Don't need Dev to fix app, cuz K8S will replace unhealthy container automatically), and autoscaling 
(Don't need Ops to adding new VM when we need it, cuz K8S have capability for automatically adding based on load)
### **Kubernetes Components**
![Kubernetes Components](pic/components-of-kubernetes.svg)
More explanation about [Kubernetes Components](https://kubernetes.io/docs/concepts/overview/components/)
### **Kubernetes Objects**
| Kubernetes Objects |
| - |
| namespaces |
| nodes |
| persistentvolumes |
| deployments |
| cronjobs |
| horizontalpodautoscalers |
| etc |
> You can issue command `kubectl api-resources` in your cluster

You can read [here](https://kubernetes.io/docs/concepts/overview/working-with-objects/kubernetes-objects/) for understanding Kubernetes Objects
### **Create Kubernetes Cluster**
1. Create with [minikube](https://minikube.sigs.k8s.io/docs/start/)
2. Create in Cloud you love (AWS, Azure, GCP, etc)
3. Create less than 2 minutes with [civo](https://www.civo.com/learn/creating-a-cluster-the-path-to-success)
### **Interaction with Kubernetes Cluster**
To install kubectl in your computer, take a look this [article](https://kubernetes.io/docs/tasks/tools/)
