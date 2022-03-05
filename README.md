# kubernetes-mongo-lab

A simple kubernetes lab for make possible the comunication between **MongoDB** and **Mongo-express**, where **mongodb** is in a "private" service and just the **mongo-express** is acessible externally.

For that lap, I've used directly kubernetes components like **Pods**, **Deployments**, **Secret** and **ConfigMap**.

#### How to run
For execute this lab, it's necessary a **Kubernetes Cluster**. For run locally, we can to use the **Minikube**.

After Minikube started, we just need to run some commands to start up the infrastructure.

We will need to apply the commands sequencially, because our **Deployments** have direct dependencies of **Secret** and **ConfigMap**

`kubectl apply -f mongodb-secret.yaml`

`kubectl apply -f mongo-configmap.yaml`

`kubectl apply -f mongodb-deployment.yaml`

`kubectl apply -f mongoexpres-deployment.yaml`

Remember, if you're using **Minikube***, run the command minikube service [SERVICE NAME] "generate" a public ip and be possible to access the service from browser.
