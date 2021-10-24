# HOMEWORK for DEVOPS & IT POSITION

create a free azure account https://azure.microsoft.com/en-us/free/ (there shouldn't be any additional charges with this task , but we're not responsible if for some reason youre getting charged)

### getting started :  
## create a kubernetes cluster on (AKS) (which stands in the free trial ) through the UI / CLI 

any other platform will be accepted but should be hosted on cloud  (not locally).



___
Install `kubectl`.

connect to the cluster and show the output of : 
```
kubectl get all 
```
----

##  1. clone the repo 
```
git clone https://github.com/Contguard/home-work.git
```
Then push it to a repo on your github account.

## 2.  create yaml files for deployment :
```
that will pull image's from your repo(see next step ), and will push it to the cluster 
you can use this tutorial as a template , (Change/remove values as needed, https://docs.microsoft.com/en-us/azure/aks/ingress-basic#run-demo-applications )

```
---
## 3. create a workflow(s) for each service  using github-actions that does that:


(TIP:
it may be easier if you test everything manually first, and then move each step, to the workflow (but for your choice): 
docker build .. 
docker push , 
kubectl apply -f .. )


 1. build's  dockerfile for each service.
 2. push the images to a container registry (dosent matter which one.. dockerhub \ azure acr \ github packages  ..),
 3. deploy app .

more info can be found here https://docs.github.com/en/actions
## 4. check that the app is functional
 ```
 tip: make sure that the dashboard service can reach the counting service when you deployed the app,
      the address to it may be different .
      so make sure to set right the value of : 
      COUNTING_SERVICE_URL 
 ```



## 5. Last step  :
determine the svc name . 
```
kubectl get svc
```

use " kubectl port-forward ... " then youll be able to reach service on your localhost.



attach a screen shot of the dashboard service . check that by refreshing the page ,  the counter incerment's  .
please add some documents the showing the proccess including screenshots of commands output , logs , and explanations . 

### BONUS IDEAS (optional) :
```
* add a LoadBalancer service \ or use an nginx ingress-controller with an ingress rule in order to have external acceess to the dashboard service.
* add a helm chart for the app
* use cert-manger & letsencrypt to add ssl cert for the dashboard app.
* build the app from source
* feel free to show more skills .. :)
```

## important: 
the code for the service's is taken from hashicorp github repo . so you may find more info that can help you to complete the task.
all files created for the task should be included in the repo. 
as mentioned , there shoudnt be any charge  but we're notresponsible for any charges .
dont hesitate to ask any questions  .
## take 3 days for the task .
## dont forget to clean everything when finished ! &  send me a link to the repo / zip file.

# good luck! 
