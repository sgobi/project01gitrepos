#for Argocd 

kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl get pods  -n argocd

kubectl get pods -n argocd

kubectl get svc argocd-server -n argocd
kubectl port-forward svc/argocd-server -n argocd --address 0.0.0.0 9090:8080
kubectl port-forward svc/argocd-server -n argocd --address 0.0.0.0 9090:80
curl -k https://localhost:9090
