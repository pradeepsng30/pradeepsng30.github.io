---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<link rel="stylesheet" href="{{ '/styles.css' | relative_url }}">
<h1>Projects</h1>
<ul>
  {% assign pages = site.pages %}
  {% for page in pages %}
      {% if page.desc %}
     <div class="page-box">
        <a class="page-title" href="{{ page.url }}">{{ page.title | default: page.name }}</a>
        <p class="page-desc">{{ page.desc }}</p>
      </div>
    {% endif %}
  {% endfor %}
</ul>