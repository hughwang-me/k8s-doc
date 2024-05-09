# YAML - Service

## 功能说明

YAML 配置参考手册 - Service

## YAML Service 配置参考
``` 
apiVersion: v1
kind: Service
metadata:
  name: myapp
spec:
  selector:
    app: myapp
  ports:
  - port: <Port>
    targetPort: <Target Port>

```
