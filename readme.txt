Dockerfile process : 
1 - docker build -t pseudo/nom-image .
2 - docker push pseudo/nom-image 

Kubernetes process :
1 - kubectl create deployment nom-deployment --image pseudo/nom-image
2 - kubectl expose deployment/nom-deployment --type LoadBalancer --port 80
3 - minikube service nom-deployment
4 - kubectl scale --replicas=6 nom-deployment 

Git process :
1 - git init 
2 - git add .
3 - git commit 
4 - git remote add origin lien-github
5 - git push -u origin master