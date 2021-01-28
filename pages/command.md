---
layout: page
title: 常用命令
description: 常用命令
keywords: command, 常用命令
comments: false
menu: 常用命令
permalink: /command/
---

> 常用命令整理

<ul class="listing">
{% for command in site.command %}
{% if command.title != "command Template" %}
<li class="listing-item"><a href="{{ site.myurl }}{{ command.url }}">{{ command.title }}<span style="font-size:12px;color:red;font-style:italic;"></span></a></li>
{% endif %}
{% endfor %}
</ul>
