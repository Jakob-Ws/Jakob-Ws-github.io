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
      <a href="{{ book.url }}">{{ book.title }} - {{ book.author }}</a> ( 
      <strong>{{ book.rating }}/10</strong>; gelesen: {{ book.date | date: "%d. %m %Y" }})
    </li>
  {% endfor %}
</ul>