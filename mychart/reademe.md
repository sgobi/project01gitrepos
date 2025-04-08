kubectl create secret docker-registry my-registry-secret \
  --docker-server=192.168.1.10:8082 \
  --docker-username=admin \
  --docker-password=123 \
  --docker-email=g2k2@live.com

#confirmation
kubectl get secret my-registry-secret -o yaml

minikube stop
minikube config set insecure-registry "192.168.1.10:8082"
minikube start


helm install mychart ./mychart
