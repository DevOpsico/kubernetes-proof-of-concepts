export IMG="yoshyn/k8s-operator-memcached:latest"; make undeploy; make docker-build && make docker-push && make deploy && sleep 5 && kubectl
pply -f config/samples/app_v1_pocproject.yaml && sleep 8 && kubectl logs $(kubectl get pod --namespace=operator-ansible-pocproject-system --no-headers | awk '{print $1}') -f --name
pace=operator-ansible-pocproject-system --container manager






KUSTOMIZE_PATH="$(pwd)/bin/kustomize" molecule test
