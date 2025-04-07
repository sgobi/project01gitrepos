  352  docker login -u admin -p 123 http://192.168.1.10:8082
  353  docker push 192.168.1.10:8082/my-flask-app:10
  354  docker tag my-flask-app:10 192.168.1.10:8082/my-flask-app:10
  355  docker push 192.168.1.10:8082/my-flask-app:10
