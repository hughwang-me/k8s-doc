# Minikube 基本使用

## 功能说明

Minikube的基本使用，https://minikube.sigs.k8s.io/docs/start/

## 命令

##### 安装：
> brew install minikube

##### 重新安装：
>brew unlink minikube
>brew link minikube

##### 启动：
>minikube start

##### 使用：

说明：需要已经安装了 `kubectl` 工具。如果没有 可以走`minikube`。
> kubectl get po -A
> 
> minikube kubectl -- get po -A
> 
> alias kubectl="minikube kubectl --"

##### 查看仪表盘：
> minikube dashboard

