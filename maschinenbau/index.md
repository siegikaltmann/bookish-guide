---
layout: site
title: Maschinenbau – Skriptum
# theme kommt aus _config.yml (theme-violet)
---

<section class="card">
  <h1>Kapitel</h1>
  <p class="muted">Alle Kapitel in logischer Reihenfolge. Klicke ein Kapitel zum Lesen.</p>
  <ol>
    {% assign chapters = site.maschinenbau | sort: 'weight' %}
    {% for ch in chapters %}
      <li>
        <a href="{{ ch.url | absolute_url }}">
          {{ ch.weight | default: forloop.index }}. {{ ch.title }}
        </a>
      </li>
    {% endfor %}
  </ol>
</section>
