---
layout: default
title: 首页
---

# {{ site.title }}

{{ site.description }}

## 最新文章

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})
*{{ post.date | date: "%Y年%m月%d日" }}*

{{ post.excerpt }}

[阅读全文 →]({{ post.url }})

---
{% endfor %}

{% if site.posts.size == 0 %}
暂无文章，敬请期待！
{% endif %}
