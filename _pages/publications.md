---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

I dabble in AR and AI.

# Selected Preprint(s)

{% for post in site.publications reversed %}
{% if post.preprint %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

-----------------

# Publications

{% for post in site.publications reversed %}
{% if post.preprint %}
   
{% else %}
{% include archive-single.html %}
{% endif %}
{% endfor %}
