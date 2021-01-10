<ul>
  {% for page in site.pages %}
  {% if page.tag %}
    <li><a href="{{ page.url | relative_url }}">{{ page.url }}</a></li>
  {% endif %}
  {% endfor %}
</ul>
