---
title: Publications
subtitle: Peer-reviewed papers and preprints
---

<p class="prose">
For an always up-to-date record, see my
<a href="https://scholar.google.com/citations?user=8LxDEiEAAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar profile</a>.
</p>

<div class="grid">
{% assign pubs = site.data.publications | sort: "year" | reverse %}
{% for pub in pubs %}
  <article class="card">
    <div class="pub">
      <div>
        <h2 class="pub-title">{{ pub.title }}</h2>
        <div class="pub-meta">{{ pub.authors | replace: ";", ", " }}</div>
        <div class="pub-meta"><strong>{{ pub.venue }}</strong> · {{ pub.year }}</div>
      </div>
      <div class="pub-links">
        {% if pub.links %}
          {% for l in pub.links %}
            <a class="badge" href="{{ l.url }}" target="_blank" rel="noopener">{{ l.label }}</a>
          {% endfor %}
        {% endif %}
      </div>
    </div>
  </article>
{% endfor %}
</div>
