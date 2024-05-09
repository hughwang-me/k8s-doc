# Kubectl 资源创建

## 功能说明

在 K8s 中，创建资源有两种方式：

- 直接使用 `kubectl run` 命令创建
- 使用 `kubectl create/apply`命令从 `YAML` 文件创建

## `kubectl run`命令

> kubectl run nginx-a --image=nginx:latest --port=80

## `kubectl create`命令

说明：仅支持新建，不支持更新。

> kubectl create -f nginx-pod.yaml

## `kubectl apply`命令

说明：更新不是所有配置属性都支持，仅支持如label等。

> kubectl apply -f nginx-pod.yaml 
