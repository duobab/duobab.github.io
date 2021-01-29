---
layout: post
title: GitLab runner搭建过程详解
categories: GitlabRunner
description: GitLab runner搭建过程详解
keywords: GitLab runner搭建过程详解
---

# docker模式下安装gitlab runner过程详解

## 1. 启动一个gitlab runner容器
docker run -d --name runner1 -v /srv/runner1/config:/etc/gitlab-runner 
-v /var/run/docker.sock:/var/run/docker.sock  gitlab/gitlab-runner:latest

## 2. 从gitlab上获取gitlab runner注册所需要的的信息
需要获取的信息有：
url
registration-token

## 3. 将gitlab runner注册到gitlab
进入容器： docker exec -it runner1 /bin/bash
执行注册命令：
  gitlab-runner register --non-interactive --url "gitlab地址" --registration-token "token" 
  --executor "docker" --docker-image maven:latest --description "runner1" 
  --tag-list "runner,runner1" --locked="false"
  
## 4. 修改gitlab runner配置
vim /srv/runner1/config/config.toml
将以下内容替换到对应节点
  volumes = ["/var/run/docker.sock:/var/run/docker.sock","/var/runcache:/mavencache:rw","/nm:/nm"]
  pull_policy = "if-not-present"
或者替换以下内容
  ["/var/run/docker.sock:/var/run/docker.sock","/var/runcache:/cache:rw"]
    pull_policy = "if-not-present"

## 5. gitlab上确认开启gitlab runner
