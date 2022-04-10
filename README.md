# cheat-sheet
```
#GO
go mod init hello - инициализировать проект
go get - выкачать зависимости
go run main.go - запустить
go build . - собрать проект в исполняемый файл

#DOCKER
docker build --tag creatiwww/devops_test_faraway:latest .
docker image ls
docker image rm devops_test:latest
docker run devops_test:latest
docker run -d -p 8080:8080 --name rest-server devops_test:latest
curl localhost:8080
docker ps
docker stop <name of container> (-all или -a)
docker exec -it c21bfac5169e sh (или /bin/bash)
docker attach c21bfac5169e -  вывод в консоль
docker tag devops_test_faraway:latest creatiwww/devops_test_faraway:latest
docker push creatiwww/devops_test_faraway:latest
docker volume rm $(docker volume ls -q)

docker network ls
docker network create cross-network
docker network prune -f
sudo docker inspect ecb4 -f "{{json .NetworkSettings.Networks }}"

#DOCKER-COMPOSE
docker-compose config
docker-compose up --build -d

#KUBECTL
kubectl config use-context minikube
kubectl get all
kubectl delete all --all

# enter running container
kubectl exec --stdin --tty devops-test-deployment-6469f9667f-4snph -- /bin/bash

#HOW TO RUN minikube
minikube delete
minikube start --vm-driver=kvm2
               --vm-driver=docker
minikube addons enable ingress               

#HOW TO INSTALL GO
исналировать go
- скачать с офф сайта https://golang.org/doc/install
- разорхивировать в usr/local/
- добавить путь до usr/local/go/bin в $GOPATH в профайл
- перезагрузить

#HOW TO INSTALL DOCKER-COMPOSE
sudo curl -L "https://github.com/docker/compose/releases/download/2.1.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

#HOW TO INSTALL GRAFANA MONITORING
https://grafana.com/api/dashboards/763/revisions/3/download # import redis dashboard
https://grafana.com/api/dashboards/6671/revisions/2/download  # import go dash

#GENERATE LOADS
for i in {1..100}; do curl http://localhost:8080; done
```

#GIT
git push https://ghp_<tocken>@github.com/creatiwww/<repository>.git
#push to github
echo "# tf" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Creatiwww/tf.git
git push -u origin main
