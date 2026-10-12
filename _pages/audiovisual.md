---
title: "Audiovisual"
permalink: /audiovisual/
author_profile: true
---

Audio-visual ethnographies and video documentation of urban research. More on [Vimeo](https://vimeo.com/{{ site.author.vimeo }}).

{% for video in site.data.videos %}
<h2>{{ video.title }}{% if video.year %} ({{ video.year }}){% endif %}</h2>
{% if video.title_en %}<p class="video__subtitle">{{ video.title_en }}</p>{% endif %}
<div class="video-embed">
  <iframe src="https://player.vimeo.com/video/{{ video.vimeo_id }}?dnt=1" title="{{ video.title | escape }}" loading="lazy" allow="fullscreen; picture-in-picture" allowfullscreen></iframe>
</div>
{% if video.description %}<p>{{ video.description }}</p>{% endif %}
{% endfor %}
