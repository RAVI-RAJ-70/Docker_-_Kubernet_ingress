# Docker_-_Kubernet_ingress

Firstly I am creating Django project.
then create Dockerfile.
then i am creating devlopment.yaml file.
then creating service.yaml file.
for host domain name im creating ingress.yaml file.

Important Command:- 
for import ingress Controller :- kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml 
for Apply file :- kubectl apply -f deployment.yaml   (Same for service file and ingress file)
for Delete file :- kubectl delete -f deployment.yaml   (Same for service file and ingress file)
for get service Status :- kubectl get svc
for get ingress service details :- kubectl get ingress -n=(your Name space name)ingress-nginx  
for get ingress service details :- kubectl get svc -n=ingress-nginx  

Note:- 1. Give permission in Django project setting.py (ALLOWED_HOSTS = ["*"])
       2. we have to Map our host before apply ingress. (put your Domain name) 
            open ur Notepad through Run as Administrator then open file then go this path (C:\Windows\System32\drivers\etc) 
----------------------------------------------------------------------------------------------------------------            
{{# localhost name resolution is handled within DNS itself.
#	127.0.0.1       localhost
#	::1             localhost

127.0.0.1 raviraaz.com  ..........................................(put ur Domain name As i put my Domain Name)
127.0.0.1 kubernetes.docker.internal
127.0.0.1 kubernetes.docker.internal
# Added by Docker Desktop))
------------------------------------------------------------------------------------------------------------------------
