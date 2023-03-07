- 镜像打包构建
    1. 打包镜像：`docker build . -t ${DockerHub_Name}/hellok8s:v1`
    2. 推送镜像：`docker push ${DockerHub_Name}/hellok8s:v1`
- 运行Pod
    1. 运行Pod：`kubectl apply -f nginx.yaml`
    2. 端口映射：`kubectl port-forward nginx-pod 4000:80`

