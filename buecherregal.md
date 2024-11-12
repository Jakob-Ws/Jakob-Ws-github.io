---
layout: default
title: Bücherregal
permalink: /bücherregal/
---

# Bücherregal

<ul>
  {% assign sorted_books = site.books | sort: 'rating' | reverse %}
  {% for book in sorted_books %}
    <li>
      <a href="{{ book.url }}">{{ book.title }}</a> - 
      <strong>{{ book.rating }}/10</strong>
      (Autor: {{ book.author }}, veröffentlicht am: {{ book.date | date: "%d. %b %Y" }})
    </li>
  {% endfor %}
</ul>