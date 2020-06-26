---
is_main: True
---
### Articles

This page will index article pages I post.

<div class="grid">
  {% assign startrow = true %}
  {% for post in site.posts %}
    <div class="grid-item">
		{% if startrow == true%}
			<div style = "width: 100%; float:left;">
				<a href="{{ post.url }}" title = "{{ post.title }}">
					<div style = "float:left; background-image:url({{ post.post_image }});">{{ post.title }}</div>
				</a>
				<div style = "width: -webkit-fill-available;">
					<p style = "text-align: center; line-height: normal;">
						{{ post.summary }}
					</p>
				</div>
			</div>
			{% assign startrow = false %}
		{% else %}
			<div style = "width: 100%; float:right;" >
				<a href="{{ post.url }}" title = "{{ post.title }}">
					<div style = "float:right; background-image:url({{ post.post_image }});">{{ post.title }}</div>
				</a>
				<div style = "width: -webkit-fill-available;" >
					<p style = "text-align: center; line-height: normal;">
						{{ post.summary }}
					</p>
				</div>
			</div>
			{% assign startrow = true %}
		{% endif %}
    </div>
  {% endfor %}
</div>