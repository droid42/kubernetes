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


### Helm

~~~~
export HELM_VERSION=v2.14.2
wget https://kubernetes-helm.storage.googleapis.com/helm-$HELM_VERSION-linux-arm.tar.gz
tar xvzf helm-$HELM_VERSION-linux-arm.tar.gz
mv linux-arm/helm /usr/local/bin/helm
rm -rf linux-arm
helm list
helm init --tiller-image=jessestuart/tiller:v2.9.0 --service-account tiller
~~~~
