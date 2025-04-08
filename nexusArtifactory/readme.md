docker login -u admin -p 123 http://192.168.1.10:8082
docker push 192.168.1.10:8082/my-flask-app:10
docker tag my-flask-app:10 192.168.1.10:8082/my-flask-app:10
docker push 192.168.1.10:8082/my-flask-app:10
