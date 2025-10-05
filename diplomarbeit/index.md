---
layout: default
title: Diplomarbeiten
# theme kommt aus defaults → theme-amber
---

<h1>Diplomarbeiten</h1>
<p class="muted">Updates sind nach Projekt gruppiert (aktuellste oben).</p>

{% assign groups = site.diplomarbeit | group_by: 'project' %}
{% assign sorted = groups | sort: 'name' %}
{% for g in sorted %}
<section class="card" style="margin-bottom:16px;">
<h2 style="margin:0 0 10px;">{{ g.name | default: 'Allgemein' }}</h2>
{% assign entries = g.items | sort: 'date' | reverse %}
<ul>
{% for item in entries %}
<li>
<a href="{{ item.url | relative_url }}">{{ item.title }}</a>
<span class="muted"> – {{ item.date | date: "%b %Y" }}</span>
</li>
{% endfor %}
</ul>
</section>
{% endfor %}
