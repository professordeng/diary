<ul>
  {% for page in site.pages %}
    {% if page.url.size == 16 %}
      <li><a href = "{{ page.url | relative_url }}">{{ title | truncate: 10, "" }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
