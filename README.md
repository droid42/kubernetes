# kubernetes

## nginx ingress

### Get source & build

https://github.com/nginxinc/kubernetes-ingress

### Install

kubectl create -f nginx-ingress-svc.yaml  -n demo

kubectl create -f nginx-ingress-dly.yaml  -n demo

kubectl get service ingress-nginx -owide -n demo
