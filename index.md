<ul>
  {% for page in site.pages %}
    {% assign title = page.url | replace_first: "/", "" | replace "/", " " | replace ".html" ""  %}
    {% if title.size == 10 %}
      <li><a href="{{ page.url | relative_url }}">{{ title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
