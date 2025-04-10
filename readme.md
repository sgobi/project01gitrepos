#for Argocd 

kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl get pods  -n argocd

ngrok http --scheme=https --host-header=rewrite https://192.168.49.2:30517kubectl get pods -n argocd

kubectl get svc argocd-server -n argocd
kubectl port-forward svc/argocd-server -n argocd --address 0.0.0.0 9090:8080
kubectl port-forward svc/argocd-server -n argocd --address 0.0.0.0 9090:80
curl -k https://localhost:9090


kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d



#ngrok

https://www.youtube.com/watch?v=SZmc5uoNCko

kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "NodePort"}}'
kubectl get svc argocd-server -n argocd
curl -k https://localhost:30517
kubectl get nodes -o wide
curl -k https://192.168.49.2:30517
ngrok http --scheme=https --host-header=rewrite https://192.168.49.2:30517
