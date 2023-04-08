{% for page in site.html_pages %}
{% if page.url != "/" %}
{% if page.not_indexing != false %}
### {{ page.title }}
`{{ page.url | absolute_url | remove: ".html" | split: "://" | last }}` -> [`{{ page.redirect.to | split: "://" | last }}`]({{ page.redirect.to }})
{% endif %}
{% endif %}
{% endfor %}