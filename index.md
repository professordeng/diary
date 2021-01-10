<ul>
  {% for page in site.pages %}
    {% if page.dir.size >= 4 %}
      <li>
        <a href="{{ page.url | relative_url }}">
          {{ page.url }}
        </a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
