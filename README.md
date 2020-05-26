# Kubernetes GoFrame 
## 介绍
kubernetes  GO 客户端与GoFrame提供接口对kubernetes相关资源的管理

## 完成功能
1. pod容器列表
2. pod websocket
3. deployment 列表
4. namespace  列表
5. service 列表

# 运行 



# 接口
  SERVER  | DOMAIN  | ADDRESS | METHOD |            ROUTE            |                        HANDLER                         |      MIDDLEWARE
|---------|---------|---------|--------|-----------------------------|--------------------------------------------------------|-----------------------|
  default | default | :80     | ALL    | /kubernetes/deployment/list | k8s/kubernetes/deployment.(*DeployMentController).List | router.MiddlewareCORS
|---------|---------|---------|--------|-----------------------------|--------------------------------------------------------|-----------------------|
  default | default | :80     | ALL    | /kubernetes/namespace/list  | k8s/kubernetes/namespace.(*NameSpaceController).List   | router.MiddlewareCORS
|---------|---------|---------|--------|-----------------------------|--------------------------------------------------------|-----------------------|
  default | default | :80     | ALL    | /kubernetes/pod/list        | k8s/kubernetes/pod.(*podws.PodController).List         | router.MiddlewareCORS
|---------|---------|---------|--------|-----------------------------|--------------------------------------------------------|-----------------------|
  default | default | :80     | ALL    | /kubernetes/pod/websocket   | k8s/kubernetes/pod.(*podws.PodWSController).Websocket  | router.MiddlewareCORS
|---------|---------|---------|--------|-----------------------------|--------------------------------------------------------|-----------------------|
  default | default | :80     | ALL    | /kubernetes/service/list    | k8s/kubernetes/service.(*ServiceController).List       | router.MiddlewareCORS
|---------|---------|---------|--------|-----------------------------|--------------------------------------------------------|-----------------------|
