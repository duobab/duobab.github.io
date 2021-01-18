---
layout: command
title: windows 常用命令
categories: command
description: windows 常用命令
keywords: windows 常用命令
---

## 查看端口是否开启
netstat -ano|findstr "9050"

## 根据 端口号 过滤所有进程
tasklist|findstr "9050"

## 根据 进程名称 过滤所有进程
tasklist|findstr "9050"

## 结束进程X
taskkill /f /t /im X.exe

## 查看共享的文件夹
NET SHARE

## 启用/禁用 ping
netsh firewall set icmpsetting 8         (启用ping)
netsh firewall set icmpsetting 8 disable (禁用ping)
