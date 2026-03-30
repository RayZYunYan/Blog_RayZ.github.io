---
layout: home
title: Home
---

Welcome back, Ray!
每一次记录都是思想的革命

{% for post in paginator.posts %}
<article class="post">
<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
<p class="post-meta">{{ post.date | date: "%B %e, %Y" }}</p>
{{ post.excerpt }}
</article>
{% endfor %}

<div class="pagination">
{% if paginator.previous_page %}
<a href="{{ paginator.previous_page_url }}">← 上一页</a>
{% endif %}

Page {{ paginator.page }} of {{ paginator.total_pages }}

{% if paginator.next_page %}
<a href="{{ paginator.next_page_url }}">下一页 →</a>
{% endif %}
</div>
