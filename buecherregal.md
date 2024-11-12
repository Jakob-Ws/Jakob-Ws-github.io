layout: default
permalink: /bücherregal/
---
# Bücherregal

<ul>
  {% assign sorted_reviews = site.books | sort: 'rating' | reverse %}
  {% for buch in sorted_books %}
    <li>
      <a href="{{ review.url }}">{{ review.title }}</a> -
      <strong>{{ review.rating }}/10</strong>
      (Autor: {{ review.author }}, gelesen am: {{ review.date | date: "%m. %b %Y" }})
    </li>
  {% endfor %}
</ul>
