<ul>
  {% for page in site.pages %}
    {% assign title = page.url | remove_first: "/" | replace "/", " " | remove ".html"  %}
    {% if title.size == 10 %}
      <li><a href="{{ page.url | relative_url }}">{{ title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
