---
layout: post
title: Spring Security 使用
categories: Spring
description: Spring Security 使用
keywords: Spring Security 使用
---

本章主要介绍Spring Security。

* * *

## 1.1 简介
目前主流的权限管理框架有Shiro 和 Spring Security。  
Shiro是 Java 领域老牌的权限管理框架, 它轻量、简单、易于集成。  
Spring Security 最初是叫Acegi Security, 由于重量级、配置繁琐、门槛高, 一直困扰着开发者, 直到 Spring Boot的出现, 这些问题统统都得到缓解。  
权限管理框架最核心的功能：认证+授权。  

* * *

## 1.2 入门
- 新建一个 Spring Boot 项目, 引入 Spring Security 依赖和 web 依赖  
`<dependency>`  
   `<groupId>org.springframework.boot</groupId>`  
   `<artifactId>spring-boot-starter-web</artifactId>`  
`</dependency>`  
`<dependency>`  
    `<groupId>org.springframework.boot</groupId>`  
    `<artifactId>spring-boot-starter-security</artifactId>`  
`</dependency>`  
- 添加一个测试的 HelloController
- 启动项目, 控制台会输出默认用户user的密码
- 访问controller层接口, 会跳转到login 页面进行认证

- 在配置文件中自定义用户名、密码
spring.security.user.name=test
spring.security.user.password=123

- 在配置类中自定义用户名、密码
需要继承WebSecurityConfigurerAdapter, 重写passwordEncoder和configure(AuthenticationManagerBuilder auth)方法

- 自定义表单登录页
需要继承WebSecurityConfigurerAdapter, 重写configure(WebSecurity web) 和 configure(HttpSecurity http) 方法

* * *
