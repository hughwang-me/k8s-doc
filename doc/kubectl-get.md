# Kubectl

## 功能说明

API 操作

## 命令

##### 获取 `Pod` 列表：
> kubectl get pods/po/pod

``` 
wanghuan•~/Documents/k8s_workspace» kubectl get pods                                                                                                                                      [14:33:58]
NAME                               READY   STATUS      RESTARTS     AGE
hello-minikube-5c898d8489-gkffb    1/1     Running     2 (9d ago)   13d
hello-minikube1-67bf99b564-6mvsg   1/1     Running     2 (9d ago)   13d
k8s-magic-box-74f99fdbfb-4c2hs     1/1     Running     0            3h30m
k8s-magic-box-74f99fdbfb-jp2fx     1/1     Running     0            3h30m
k8s-magic-box-74f99fdbfb-kwzz8     1/1     Running     0            3h30m
my-nginx-1                         0/1     Completed   0            10d
nginx-bf5d5cf98-b9zbm              1/1     Running     1 (9d ago)   11d
wanghuan-app-a-545d6b8586-hsj48    1/1     Running     2 (9d ago)   13d
```

##### 获取 `Service` 列表：
> kubectl get services/service/svc

``` 
wanghuan•~/Documents/k8s_workspace» kubectl get svc                                                                                                                                       [14:47:54]
NAME              TYPE           CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
hello-minikube    NodePort       10.99.193.221   <none>        8080:30504/TCP   13d
hello-minikube1   LoadBalancer   10.108.213.26   <pending>     8082:32656/TCP   13d
k8s-magic-box     LoadBalancer   10.98.108.164   <pending>     8080:30953/TCP   4h5m
kubernetes        ClusterIP      10.96.0.1       <none>        443/TCP          13d
nginx             NodePort       10.101.14.232   <none>        80:31040/TCP     11d
wanghuan-app-a    NodePort       10.103.95.116   <none>        8080:31344/TCP   13d
```

##### 获取 `Node` 列表：
> kubectl get nodes/node/no

``` 
wanghuan•~/Documents/k8s_workspace» kubectl get node                                                                                                                                      [14:47:58]
NAME       STATUS   ROLES           AGE   VERSION
minikube   Ready    control-plane   13d   v1.30.0
```

##### 获取 `Replicas` 列表：
> kubectl get rs

``` 
wanghuan•~/Documents/k8s_workspace» kubectl get rs                                                                                                                                    [14:47:58]
NAME                         DESIRED   CURRENT   READY   AGE
hello-minikube-5c898d8489    1         1         1       13d
hello-minikube1-67bf99b564   1         1         1       13d
k8s-magic-box-69967bcdb5     0         0         0       4h31m
k8s-magic-box-74f99fdbfb     3         3         3       3h51m
nginx-bf5d5cf98              1         1         1       11d
wanghuan-app-a-545d6b8586    1         1         1       13d
```

##### 获取 `deploy` 列表：
> kubectl get deployments/deploy

``` 
wanghuan•~/Documents/k8s_workspace» kubectl get deploy                                                                                                                                    [15:04:05]
NAME              READY   UP-TO-DATE   AVAILABLE   AGE
hello-minikube    1/1     1            1           13d
hello-minikube1   1/1     1            1           13d
k8s-magic-box     3/3     3            3           4h40m
nginx             1/1     1            1           11d
wanghuan-app-a    1/1     1            1           13d
```
