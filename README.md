# kubernetes-proof-of-concepts
This repositories stores all the k8s POCs prior to real implementations.

`make docker-build docker-push IMG=yasseur/operator-ansible-pocproject:latest`

`minikube start`

`make install`

`export IMG="yasseur/operator-ansible-pocproject:latest"`

`make deploy`

`kubectl get deployment --namespace=operator-ansible-pocproject-system`

Should have 1 pods. This pods has 2 containers (manager & kube-rbac-proxy).

`kubectl logs $(kubectl get pod --namespace=operator-ansible-pocproject-system --no-headers | awk '{print $1}') -f --namespace=operator-ansible-pocproject-system --container manager`

`kubectl apply -f config/samples/app_v1_pocproject.yaml`
`kubectl get pocprojects.app.devopsico.com`

`kubectl describe pp pocproject-sample`

`make undeploy`
