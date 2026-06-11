---
layout: page
title: "Blog"
permalink: /blog/
---

Short writeups of troubleshooting, lessons learned, and project notes.

{% for post in site.posts %}
- **[{{ post.title }}]({{ post.url | relative_url }})** — {{ post.date | date: "%b %d, %Y" }}
{% endfor %}
