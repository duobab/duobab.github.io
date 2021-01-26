---
layout: post
title: windows和linux共享存储方案
categories: other
description: windows和linux共享存储方案
keywords: windows和linux共享存储方案
---

# windows和linux共享存储方案

## 1. 在windows环境下将目录test开启共享

## 2. 在linux环境下挂载共享目录
首先保证linux能与window连通 (能ping通)
yum install samba
mount -t cifs -o username=""Administrator"" //windows-ip/test /home/test"
