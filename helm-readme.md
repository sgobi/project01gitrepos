helm package ./my-flask-app
helm repo add my-nexus-repo1 http://192.168.1.10:8081/repository/myprojecthelmc/ --username admin --password 123
curl -u admin:123 --upload-file ./my-flask-app-0.1.0.tgz "http://192.168.1.10:8081/repository/myprojecthelmc/my-flask-app-0.1.0.tgz"
helm search repo my-nexus-repo1/my-flask-app
