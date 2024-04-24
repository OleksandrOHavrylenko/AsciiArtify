# ArgoCD setup manual

k3d cluster create argo  
kubectl cluster-info  
k get all -A  

kubectl create namespace argocd  
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml  
k get all -n argocd  
k get po -n argocd -w  
kubectl port-forward svc/argocd-server -n argocd 8080:443&  

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo  

go to localhost:8080 

input

admin = admin  
password = password from previous step  

![Image](./images/demo_argocd.gif)


