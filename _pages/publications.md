---
title: "Choi Lab - Publications"
layout: default
excerpt: "Our research publications"
permalink: /publications/
---

# Publications

<ul>
{% for pub in site.data.publications %}
  <li>{{ pub.year }}. {{ pub.authors }}. <strong>{{ pub.title }}</strong>. {{ pub.journal }}.</li>
{% endfor %}
</ul>
