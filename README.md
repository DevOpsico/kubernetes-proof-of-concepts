# kubernetes-proof-of-concepts
This repositories stores all the k8s POCs prior to real implementations.

`make docker-build docker-push IMG=yasseur/operator-ansible-pocproject:latest`

`minikube start`

`make install`

`export IMG="yasseur/operator-ansible-pocproject:latest"`

`make deploy`

`kubectl get deployment --namespace=operator-ansible-pocproject-system`
`kubectl get pod --namespace=operator-ansible-pocproject-system`

Should have 1 pods. This pods has 2 containers (manager & kube-rbac-proxy).

`kubectl exec operator-ansible-pocproject-controller-manager-69694464b6-8xwgq -ti --namespace=operator-ansible-pocproject-system --container manager -- /bin/sh`

`kubectl apply -f config/samples/app_v1_pocproject.yaml`
`kubectl get pocprojects.app.devopsico.com`

`kubectl describe pp pocproject-sample`

`make undeploy`
