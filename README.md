# Kubernetes

#To install the metrics server

kubectl apply -f https://raw.githubusercontent.com/ACloudGuru-Resources/content-cka-resources/master/metrics-server-components.yaml 
kubectl get --raw /apis/metrics.k8s.io #To get the response of the APIs

#to get the status 

//nodes

kubectl top nodes --sort-by=cpu 

//Pods

kubectl top po -A --sort-by=cpu

//Delete the stuck terminating resources

https://stackoverflow.com/questions/52369247/namespace-stuck-as-terminating-how-i-removed-it/57726448#57726448


//Paste the data in Vi

Set vi to 'paste' mode by hitting :, and then typing set paste (ENTER). Then switch back to INSERT mode by hitting i.


//Change the namespace
kubectl config set-context --current --namespace=devtest


//update the label of the pod/service/deployment
kubectl label deployment nginx-deployment "server=nginix-webserver-1.14.2" --overwrite -n devtest


# List Events sorted by timestamp
kubectl get events --sort-by=.metadata.creationTimestamp

# Compares the current state of the cluster against the state that the cluster would be in if the manifest was applied.
kubectl diff -f ./my-manifest.yaml