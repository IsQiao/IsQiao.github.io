---
title: 
date: 2020-12-18 00:00:00 Z
categories:
- K8s
layout: post
---

# K8s常用命令

## get
*列出资源*

```
kubectl get services
kubectl get deployments // 查看部署
kubctl get nodes // 节点信息
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
kubectl get pods -l run=kubernetes-bootcamp
```

## expose
*暴露端口*

```
kubectl expose deployment/kubernetes-bootcamp --type="NodePort" --port 8080
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
