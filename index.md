{% assign pages_by_dir = site.pages | group_by_exp : "page", "page.dir" %}
{% for group in pages_by_dir %}

{% unless group.name == '/' or group.name == '/assets/css/' %}
<h3>{{ group.name | remove: "/" }}</h3>
<ul>
  {% for page in group.items %}
    <li><a href = "{{ page.url | relative_url }}">{{ page.name | truncate: 5, "" | replace: "-", " - " }}</a></li>
  {% endfor %}
</ul>
{% endunless %}

{% endfor %}