---
layout: default
title: Bücherregal
permalink: /bücherregal/
---

# Bücherregal

<p>Sortieren nach: 
  <a href="?sort=rating">Bewertung</a> | 
  <a href="?sort=date">Neuestes</a>
</p>

<ul>
  {% assign sort_order = page.url | split: '?' | last | split: '=' | last %}
  {% if sort_order == "date" %}
    {% assign sorted_books = site.books | sort: 'date' | reverse %}
  {% else %}
    {% assign sorted_books = site.books | sort: 'rating' | reverse %}
  {% endif %}

  {% for book in sorted_books %}
    <li>
      <a href="{{ book.url }}">{{ book.title }} - {{ book.author }}</a> ( 
      <strong>{{ book.rating }}/10</strong>; gelesen: {{ book.date | date: "%d. %m %Y" }})
    </li>