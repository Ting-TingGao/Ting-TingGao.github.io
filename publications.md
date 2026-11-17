---
layout: default
title: Publications
description: Publications by Ting-Ting Gao.
---

# Publications

<p>See also my <a href="{{ site.scholar }}" target="_blank" rel="noopener">Google Scholar profile</a>.</p>

{% assign pubs = site.data.publications %}
{% assign years = pubs | map: "year" | uniq | sort | reverse %}

{% for year in years %}
  <div class="year-head">{{ year }}</div>
  <ul class="pub-list">
  {% for pub in pubs %}
    {% if pub.year == year %}
    <li class="pub{% if pub.cover %} has-cover{% endif %}">
      <div class="pub-main">
        <div class="pub-title">
          {% if pub.link %}<a href="{{ pub.link }}" target="_blank" rel="noopener">{{ pub.title }}</a>{% else %}{{ pub.title }}{% endif %}
          {% if pub.status == "review" %}<span class="badge review">Under review</span>{% endif %}
          {% if pub.status == "submitted" %}<span class="badge submitted">Submitted</span>{% endif %}
          {% if pub.status == "preparation" %}<span class="badge preparation">In prep</span>{% endif %}
        </div>
        <div class="pub-authors">{{ pub.authors }}</div>
        <div class="pub-venue"><em>{{ pub.venue }}</em>{% if pub.details %}, {{ pub.details }}{% endif %}</div>
      </div>
      {% if pub.cover %}<figure class="pub-cover">{% if pub.cover_link %}<a href="{{ pub.cover_link }}" target="_blank" rel="noopener">{% endif %}<img src="{{ pub.cover | relative_url }}" alt="{{ pub.cover_caption | default: pub.venue }} — {{ pub.title }}" loading="lazy">{% if pub.cover_link %}</a>{% endif %}{% if pub.cover_caption %}<figcaption>{{ pub.cover_caption }}</figcaption>{% endif %}</figure>{% endif %}
    </li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}
