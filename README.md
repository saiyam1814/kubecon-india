# kubecon-india

### Create Kubernetes cluster 
Create any Kubernetes clsuter 

### Install cert managet
`kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.16.2/cert-manager.yaml`

### Install Nginx ingress contrller 
`kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.9.4/deploy/static/provider/cloud/deploy.yaml`


### Create Two vclusters 
```
vcluster create kubecon-demo -f vcluster.yaml
vcluster create kubecon-demo2

```

### Connect to kubecon-demo and switch the context and create application

```
kubectl apply -f app.yaml
kubectl apply -f issuer.yaml
kubecl apply -f ingress.yaml
kubectl apply -f certificate.yaml
```

### Create the cluster policy for Kyverno on 
`kubectl apply -f clusterpolicy.yaml'

### Connect to kubecon-demo2
`kubectl create service nodeport demo --tcp 80:80`

