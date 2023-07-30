#!/bin/bash

sudo apt-get update -y

sudo apt-get install curl wget apt-transport-https virtualbox virtualbox-ext-pack -y

echo "First install docker"
sudo apt update && apt -y install docker.io

echo "Start and Enable Docker and change permission"
sudo systemctl start docker

sudo systemctl enable docker

sudo chmod 666 /var/run/docker.sock

sudo apt update -y 

sudo apt upgrade -y

wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

sudo cp minikube-linux-amd64 /usr/local/bin/minikube

sudo chmod +x /usr/local/bin/minikube

minikube version

curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

chmod +x kubectl

sudo mv kubectl /usr/local/bin/

kubectl version -o yaml

minikube start 

minikube status



NOTE !  
IF YOU ARE RUNNING MINIKUBE AS NORMAL USER DO THIS BELLOW

1. After run this ABOVE script without root:: minikube start
2. Then run this:: sudo usermod -aG docker webserver && newgrp docker
3. Then run again without root user::  minikube start
