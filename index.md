<ul>
  {% for page in site.pages %}
    {% assign title = page.url | remove_first: "/" | replace "/", " " %}
    {% if title.size == 15 %}
      <li><a href = "{{ page.url | relative_url }}">{{ title | truncate: 10, "" }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
