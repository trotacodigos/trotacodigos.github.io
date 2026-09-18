---
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

## About Me
I am a postdoc at the AI-Bio Convergence Research Institute and a visiting professor at Soongsil University.

My work centers on **evaluating language models**, with a particular emphasis on **multilingual capability and reliability**. I develop **theoretically grounded and empirically robust evaluation frameworks** by bridging Linguistics, Translation Studies, and Computer Science.

I received my PhD in Language Technology from Universitat Pompeu Fabra (UPF), where I also completed my master's in Translation Studies, both under the supervision of Carme Colominas Ventura. Before moving to Barcelona, I trained in Spanish translation and interpretation at the Graduate School of Interpretation and Translation (GSIT) of Hankuk University of Foreign Studies (HUFS). I hold a bachelor's degree from HUFS in Spanish Philology and English Translation Studies.


## Latest News

{% assign now_ts = "now" | date: "%s" | plus: 0 %}
{% assign one_year_ago = now_ts | minus: 31536000 %}

<ul>
{% for post in site.posts %}
  {% assign post_ts = post.date | date: "%s" | plus: 0 %}
  {% if post_ts >= one_year_ago %}
    <li>
      <strong>{{ post.date | date: "%Y.%m" }}</strong> —
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>

<p><a href="/year-archive/">→ more</a></p>
