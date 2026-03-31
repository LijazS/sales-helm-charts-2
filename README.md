TO RUN 

kubectl create namespace sales-gateway-ns
kubectl create namespace sales-test-ns
kubectl label namespace sales-test-ns shared-gateway=true --overwrite

helm install sales-app -f values.yaml .


Deployment order:

1 namespace
2 secrets
3 configmaps
4 apply storage class
5 database
6 deployments
7 services
8 gateway - skip