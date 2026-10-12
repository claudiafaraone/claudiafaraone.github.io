---
title: "Publications"
permalink: /publications/
author_profile: true
---

The full list is also available on the [IRIS repository]({{ site.author.iris }}) of Università G. d'Annunzio Chieti-Pescara and on [Google Scholar]({{ site.author.googlescholar }}).

{% for group in site.data.publications %}[{{ group.group }}](#{{ group.group | slugify }}){% unless forloop.last %} · {% endunless %}{% endfor %}

{% for group in site.data.publications %}
<h2 id="{{ group.group | slugify }}">{{ group.group }}</h2>
<ul class="pub-list">
{% for pub in group.items %}
  <li>
    {{ pub.authors | replace: "Faraone C.", "<strong>Faraone C.</strong>" }} ({{ pub.year }}).
    <em>{{ pub.title }}</em>.
    {% if pub.venue %}{% if group.group == "Book chapters" %}In: {% endif %}{{ pub.venue }}{% if pub.details %}, {{ pub.details }}{% endif %}.{% elsif pub.details %}{{ pub.details }}.{% endif %}
    {% if pub.publisher %}{{ pub.publisher }}.{% endif %}
    <span class="pub__links">
      {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}">DOI</a>{% endif %}
      {% if pub.pdf %}<a href="{{ pub.pdf }}">PDF</a>{% endif %}
      {% if pub.iris %}<a href="{{ pub.iris }}">IRIS</a>{% endif %}
    </span>
  </li>
{% endfor %}
</ul>
{% endfor %}
