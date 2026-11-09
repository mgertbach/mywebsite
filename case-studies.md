---
title: Case Studies
# header: Simple Jekyll {}
# summary: A Jekyll site powered by Simple.css
permalink: /case-studies/
layout: collection
---

<ul id="case-studies">
{% for case_study in site.case-studies %}
  <li class="case-studies__item">
    <div class="case-studies__item-image"><img src="{{ case_study.image }}" alt="Alt text"></div>
    <div class="case-studies__item-details">
      <h2 class="type-text size-large weight-semibold">{{ case_study.title }}</h2>
      <p class="type-text size-regular">{{ case_study.description }}</p>
      <a class="type-text size-regular weight-medium" href="{{ case_study.url }}">Read the case study</a>
    </div>
  </li>
{% endfor %}
</ul>
