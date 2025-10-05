---
layout: default
title: Maschinenbau – Skriptum
# theme kommt aus defaults → theme-violet
---

<section class="card">
<h1>Kapitel</h1>
<p class="muted">Alle Kapitel in logischer Reihenfolge.</p>
<ol>
{% assign chapters = site.maschinenbau | sort: 'weight' %}
{% for ch in chapters %}
<li><a href="{{ ch.url | relative_url }}">{{ ch.weight | default: forloop.index }}. {{ ch.title }}</a></li>
{% endfor %}
</ol>
</section>
