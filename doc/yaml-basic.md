# Kubectl YAML

## 功能说明

YAML 文件基本

## 命令

##### 获取支持的版本信息：
> kubectl api-versions

``` 
 wanghuan•~/Documents/k8s_workspace» kubectl api-versions                                                                                                                                  [15:53:03]
admissionregistration.k8s.io/v1
apiextensions.k8s.io/v1
apiregistration.k8s.io/v1
apps/v1
authentication.k8s.io/v1
authorization.k8s.io/v1
autoscaling/v1
autoscaling/v2
batch/v1
certificates.k8s.io/v1
coordination.k8s.io/v1
discovery.k8s.io/v1
events.k8s.io/v1
flowcontrol.apiserver.k8s.io/v1
flowcontrol.apiserver.k8s.io/v1beta3
metrics.k8s.io/v1beta1
networking.k8s.io/v1
node.k8s.io/v1
policy/v1
rbac.authorization.k8s.io/v1
scheduling.k8s.io/v1
storage.k8s.io/v1
v1
```

##### 利用`explain`查看指令和参数含义

用来查看某一个配置的含义

> kubectl explain [path]
> 
> eg. kubectl explain service.spec
> 
> eg. kubectl explain deployment.spec.template.spec.containers

##### 利用`help`查看指令和参数含义

>kubectl create deployment --help


##### 利用`--dry-run`输出参考yaml

>kubectl create deployment nginx-test-dry-run --image=nginx:latest --dry-run=client -o yaml

- --dry-run=client -o yaml 将在本地模拟执行命令，并将模拟执行结果以YAML格式输出。
- --dry-run=server -o yaml 将命令请求发送到服务器，并由服务器模拟执行命令，返回经过服务器验证的YAML格式的资源定义。


``` 
apiVersion: apps/v1
kind: Deployment
metadata:
  creationTimestamp: null
  labels:
    app: nginx-test-dry-run
  name: nginx-test-dry-run
spec:
  replicas: 1
  selector:
    matchLabels:
      app: nginx-test-dry-run
  strategy: {}
  template:
    metadata:
      creationTimestamp: null
      labels:
        app: nginx-test-dry-run
    spec:
      containers:
      - image: nginx:latest
        name: nginx
        resources: {}
status: {}
```
