---
layout: post
title: code-server 搭建过程详解
categories: code-server
description: code-server 搭建过程详解
keywords: code-server 搭建过程详解
---

本章介绍如何安装code-server。

* * *

## 1.1 简介

VS Code是一个本地版的IDE, code-server则是一个web版IDE, 官方对code-server的介绍是 "Run VS Code on any machine anywhere and access it in the browser."。  
web版IDE的好处主要有：  
- 部署在服务器端, 在任何地方、任何设备通过浏览器即可使用。  
- 部署在服务器端, 使用云服务器加速测试、编译、下载依赖等速度。  
- 所有密集任务都在服务器上进行, 旅途中保证本地设备续航能力。  

* * *

## 1.2 安装部署

### 1.2.1 使用docker部署
- 在宿主机上创建一个存放code-server配置的文件夹  
`mkdir -p /home/cs-config/username/.config/code-server`
- 启动code server容器  
`docker run -itd \ `  
`--name username-cs-8084 \ `   
`-p 8084:8080 \ `    
`-v "/home/cs-config/username/.config:/root/.config" \`  
`-v "/home/coder:/home/coder/project" \`  
`-u "$(id -u):$(id -g)" \`  
`codercom/code-server:latest`
- 编辑宿主机上的code-server的配置文件，可以更新认证密码  
`vim /home/cs-config/username/.config/code-server/config.yaml`
- 可以修改code server auth页面  
`vim /usr/lib/code-server/src/browser/pages/login.html`

### 1.2.2 使用脚本部署
- 最低配置   
--   1G 内存  
--   2核 CPU
- 脚本安装(支持Linux, macOS and FreeBSD)
`curl -fsSL https://code-server.dev/install.sh | sh`

* * *

## 1.3 参考资料
[code-server官方开源地址](https://github.com/cdr/code-server) 

* * *
