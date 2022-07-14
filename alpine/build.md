# 构建镜像流程

## 1.创建Dockerfile
```
mkdir -p ~/openjdk8/Dockerfile
cd ~/openjdk8
vim Dockerfile
```
复制 /openjdk8-docker/alpine/Dockerfile 里的内容到Dockerfile中

## 2.执行构建

```
cd ~/openjdk8

docker build -t openjdk-8u292-alpine .

```
国内服务器构建速度很慢，很容易失败，得多构建几次


## 3.发布到镜像仓库

```
docker tag openjdk-8u292-alpine:latest ${镜像仓库地址}/openjdk-8u292-alpine:latest

docker push openjdk-8u292-alpine:latest ${镜像仓库地址}/openjdk-8u292-alpine:latest

```
