# Kubectl 资源管理 <small>获取资源描述</small>

## 功能说明

获取资源描述

## 命令

获取指定资源的实例的详细描述：
> kubectl describe [type] [name]


## 示例

获取 某一`Pod`的描述信息：
> kubectl describe pod k8s-magic-box-74f99fdbfb-jp2fx

``` 
 wanghuan•~/Documents/k8s_workspace» kubectl describe pod k8s-magic-box-74f99fdbfb-jp2fx                                                                                                   [15:02:13]
Name:             k8s-magic-box-74f99fdbfb-jp2fx
Namespace:        default
Priority:         0
Service Account:  default
Node:             minikube/192.168.49.2
Start Time:       Wed, 08 May 2024 11:03:49 +0800
Labels:           app=k8s-magic-box
                  pod-template-hash=74f99fdbfb
Annotations:      <none>
Status:           Running
IP:               10.244.0.36
IPs:
  IP:           10.244.0.36
Controlled By:  ReplicaSet/k8s-magic-box-74f99fdbfb
Containers:
  k8s-magic-box:
    Container ID:   docker://db5de0eb017a9a93e37c0ea78a0e961adb28fe3dc1c2cc5e56f66c49face690a
    Image:          k8s-magic-box:1.1
    Image ID:       docker://sha256:0cb32c4f6e50497784d9dbc8eca63ee6a8e1d3a901e4a998b2fb9ec93016bedf
    Port:           80/TCP
    Host Port:      0/TCP
    State:          Running
      Started:      Wed, 08 May 2024 11:03:51 +0800
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from kube-api-access-s4xlj (ro)
Conditions:
  Type                        Status
  PodReadyToStartContainers   True 
  Initialized                 True 
  Ready                       True 
  ContainersReady             True 
  PodScheduled                True 
Volumes:
  kube-api-access-s4xlj:
    Type:                    Projected (a volume that contains injected data from multiple sources)
    TokenExpirationSeconds:  3607
    ConfigMapName:           kube-root-ca.crt
    ConfigMapOptional:       <nil>
    DownwardAPI:             true
QoS Class:                   BestEffort
Node-Selectors:              <none>
Tolerations:                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                             node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:                      <none>
```
