---
title: Quote
layout: list
permalink: "quote/{% if pagination.pageNumber > 0 %}{{ pagination.pageNumber | plus: 1 }}{% endif %}/index.html"
pagination:
  size: 2
  reverse: true
  alias: quotes
  data: collections.quote
---

{% for quote in quotes %}
<article class="list">
<a href="{{ quote.url }}">
<header class="list-header">
<h2>{{ quote.data.title }}</h2>
</header>
<div class="list-content">
<h3>
{{ quote.templateContent }}
</h3>
</div>
</a>
</article>
{% endfor %}
