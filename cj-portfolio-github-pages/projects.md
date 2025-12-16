---
title: Projects
subtitle: Selected microscopy development projects with figures and summaries
---

<div class="grid">
  {% assign sorted = site.projects | sort: "order" %}
  {% for p in sorted %}
  <article class="card">
    <div class="pub">
      <div>
        <h2 class="pub-title" style="margin-top:0;"><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h2>
        <div class="pub-meta">{{ p.tagline }}</div>
        <div class="meta-row" style="margin-top:10px;">
          {% if p.keywords %}{% for k in p.keywords %}<span class="chip">{{ k }}</span>{% endfor %}{% endif %}
        </div>
      </div>
      <div class="pub-links">
        <a class="badge" href="{{ p.url | relative_url }}">View</a>
      </div>
    </div>
  </article>
  {% endfor %}
</div>
