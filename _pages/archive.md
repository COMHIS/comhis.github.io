---
layout: archive
title: "Posts"
permalink: /posts/
author_profile: false
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/landing2.png
---

{% for post in site.posts %}
  {% include archive-single.html %}
{% endfor %}
