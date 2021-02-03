---
layout: post
title: code server搭建过程详解
categories: codeserver
description: code server搭建过程详解
keywords: code server搭建过程详解
---

# docker模式搭建code server

## 1. 在宿主机上创建存放code server配置的文件夹
mkdir -p /home/cs-config/username/.config/code-server

## 2. 启动code server容器
docker run -itd --name username-cs-8084 -p 8084:8080 \
  -v "/home/cs-config/username/.config:/root/.config" \
  -v "/home/coder:/home/coder/project" \
  -u "$(id -u):$(id -g)" \
  codercom/code-server:latest
  
## 3. 编辑宿主机上的code server配置文件，可以修改认证密码
vim /home/cs-config/username/.config/code-server/config.yaml

## 4. 自定义code server auth页面
/usr/lib/code-server/src/browser/pages/login.html
