---
title: "News"
layout: textlay
excerpt: "Alpha-VLLM team at Leiden University."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
{{ article.date }} <br> {{ article.headline | markdownify}}
{% endfor %}
