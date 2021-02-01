---
layout: page
title: 名站导航
description: 名站导航
keywords: 名站导航
comments: false
menu: 名站导航
permalink: /website/
---

#### 常用
<ul>
{% for ws in site.data.website1 %}
<li><a href="{{ ws.url }}" target="_blank">{{ ws.name }}</a></li>
{% endfor %}
</ul>

#### 技术学习
<ul>
{% for ws in site.data.website2 %}
<li><a href="{{ ws.url }}" target="_blank">{{ ws.name }}</a></li>
{% endfor %}
</ul>

#### 购物
<ul>
{% for ws in site.data.website3 %}
<li><a href="{{ ws.url }}" target="_blank">{{ ws.name }}</a></li>
{% endfor %}
</ul>

#### 视频
<ul>
{% for ws in site.data.website4 %}
<li><a href="{{ ws.url }}" target="_blank">{{ ws.name }}</a></li>
{% endfor %}
</ul>

#### 其它



