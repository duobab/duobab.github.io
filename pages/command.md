---
layout: page
title: 猜你喜欢
description: 猜你喜欢
keywords: 猜你喜欢
menu: 猜你喜欢
permalink: /command/
---

<ul class="listing">
{% for command in site.command %}
{% if command.title != "command Template" %}
<li class="listing-item"><a href="{{ site.myurl }}{{ command.url }}">{{ command.title }}<span style="font-size:12px;color:red;font-style:italic;"></span></a></li>
{% endif %}
{% endfor %}
</ul>
