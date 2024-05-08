# Minikube <small>service</small>

## 功能说明

Minikube 网络转发

## 命令

> minikube service [svc name]

说明：需要先执行 `kubectl get svc` 获取`service`列表，根据`name`建立转发。

> kubectl get svc

```
wanghuan•~/Documents/k8s_workspace» kubectl get svc                                                                                                                                       [14:38:35]
NAME              TYPE           CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
hello-minikube    NodePort       10.99.193.221   <none>        8080:30504/TCP   13d
hello-minikube1   LoadBalancer   10.108.213.26   <pending>     8082:32656/TCP   13d
k8s-magic-box     LoadBalancer   10.98.108.164   <pending>     8080:30953/TCP   4h1m
kubernetes        ClusterIP      10.96.0.1       <none>        443/TCP          13d
nginx             NodePort       10.101.14.232   <none>        80:31040/TCP     11d
wanghuan-app-a    NodePort       10.103.95.116   <none>        8080:31344/TCP   13d
```

## 示例

> minikube service k8s-magic-box

``` 
-> % minikube service k8s-magic-box                                                                                                                                                                ✘
|-----------|---------------|-------------|---------------------------|
| NAMESPACE |     NAME      | TARGET PORT |            URL            |
|-----------|---------------|-------------|---------------------------|
| default   | k8s-magic-box |        8080 | http://192.168.49.2:30953 |
|-----------|---------------|-------------|---------------------------|
🏃  为服务 k8s-magic-box 启动隧道。
|-----------|---------------|-------------|------------------------|
| NAMESPACE |     NAME      | TARGET PORT |          URL           |
|-----------|---------------|-------------|------------------------|
| default   | k8s-magic-box |             | http://127.0.0.1:62311 |
|-----------|---------------|-------------|------------------------|
🎉  正通过默认浏览器打开服务 default/k8s-magic-box...
❗  因为你正在使用 darwin 上的 Docker 驱动程序，所以需要打开终端才能运行它
```
