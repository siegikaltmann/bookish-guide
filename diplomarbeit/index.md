---
layout: site
title: Diplomarbeiten
# theme kommt aus _config.yml (theme-amber)
---

<h1>Diplomarbeiten</h1>
<p class="muted">Updates sind nach Projekt gruppiert. Die neuesten Einträge stehen oben.</p>

{% assign groups = site.diplomarbeit | group_by: 'project' %}
{% assign groups_sorted = groups | sort: 'name' %}

{% for g in groups_sorted %}
  <section class="card" style="margin-bottom:16px;">
    <h2 style="margin:0 0 10px;">{{ g.name | default: 'Allgemein' }}</h2>

    {% assign entries = g.items | sort: 'date' | reverse %}
    <ul>
      {% for item in entries %}
        <li>
          <a href="{{ item.url | absolute_url }}">{{ item.title }}</a>
          {% if item.date %}<span class="muted"> – {{ item.date | date: "%d.%m.%Y" }}</span>{% endif %}
        </li>
      {% endfor %}
    </ul>
  </section>
{% endfor %}
