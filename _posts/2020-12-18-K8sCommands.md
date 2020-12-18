---
title: K8scommands
date: 2020-12-18 00:00:00 Z
categories:
- K8s
layout: post
---

# K8s常用命令

## set

```
kubectl set image deployments/kubernetes-bootcamp kubernetes-bootcamp=jocatalin/kubernetes-bootcamp:v2 // 更新镜像id 会滚动更新
```

## scale
```
kubectl scale deployments/kubernetes-bootcamp --replicas=4 // 修改复制品数量
```

## get
*列出资源*

```
kubectl get pods // 列出pods
kubectl get services
kubectl get deployments // 查看部署
kubctl get nodes // 节点信息
kubectl get pods -l run=kubernetes-bootcamp
kubectl get rs // ReplicaSet信息
kubectl get pods -o wide
``` 

## create

```
kubectl create deployment {name} —image={image_src} // 创建一个部署
```

## label

```
kubectl label pod $POD_NAME app=v1
```

## exec 

```
kubectl exec $POD_NAME env
kubectl exec -ti $POD_NAME bashcaca
```

## describe

```
kubectl describe services/kubernetes-bootcamp
kubectl describe deployment
kubectl describe pods // pods 信息
```

## expose
**代理服务器 暴露api 可以通过curl [http://localhost:8001/version](http://localhost:8001/version) 查看信息**

```
kubectl expose deployment/kubernetes-bootcamp --type="NodePort" --port 8080

curl http://localhost:8001/api/v1/namespaces/default/pods/$POD_NAME/proxy/
```

## 其他

```
kubectl version // 客户端版本和服务端版本信息
kubectl cluster-info // 集群信息
kubectl cluster-info dump // 集群调剂和诊断
minikube version
minikube start // 创建一个集群
kubectl version // 客户端版本和服务端版本信息
kubectl cluster-info // 集群信息
kubectl cluster-info dump // 集群调剂和诊断
```
