# kubernetes on arm

Raspberry pi 3 (Raspian arm32) and Pine A64 (Armbian arm64)

## nginx ingress

### Get source & build

https://github.com/nginxinc/kubernetes-ingress

### Install

kubectl create namespace demo

kubectl create -f nginx-ingress-svc.yaml  -n demo

kubectl create -f nginx-ingress-dly.yaml  -n demo

kubectl get service ingress-nginx -owide -n demo
