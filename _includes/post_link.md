{% assign post_title = include.title %}
{% for post in site.posts %}
  {% if post.title == post_title %}
    [{{ post.title}}]({{ post.url | relative_url }})
  {% endif %}
{% endfor %}
