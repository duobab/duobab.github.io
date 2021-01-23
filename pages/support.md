---
layout: page
title: 技术支持
description: 搭建网站, 搭建博客, 朵芭比学园, 技术支持
keywords: 搭建网站, 搭建博客, 朵芭比学园, 技术支持
comments: false
menu: 技术支持
permalink: /support/
---

如果您有搭建网站、博客、软件开发等需求,请发邮件联系我们。


## 联系

<ul>
{% for website in site.data.social %}
<li>{{website.sitename }}：<a href="{{ website.url }}" target="_blank">{{ website.name }}</a></li>
{% endfor %}

<!--  
<li>
微信公众号：<br />
<img style="height:192px;width:192px;border:1px solid lightgrey;" src="{{ assets_base_url }}/assets/images/qrcode.jpg" alt="朵芭比学园" />
</li>
-->

</ul>
