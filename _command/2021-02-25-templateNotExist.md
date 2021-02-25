---
layout: command
title: 模板异常
categories: 猜你喜欢
description: org.thymeleaf.exceptions.TemplateInputException: Error resolving template , template might not exist or might not be accessible by any of the configured Template Resolvers
keywords: org.thymeleaf.exceptions.TemplateInputException: Error resolving template , template might not exist or might not be accessible by any of the configured Template Resolvers
---

# org.thymeleaf.exceptions.TemplateInputException: Error resolving template , template might not exist or might not be accessible by any of the configured Template Resolvers

使用SpringBoot+Thyemleaf开发时, 如果controller层方法返回非json数据, 默认会找该方法返回值+.html 页面  
解决方式如下：  
-  准备一个方法返回值+.html 页面文件
-  或者在该方法上加上@ResponseBody注解
-  或者在类上加上@RestController注解
