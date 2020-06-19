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
					<img style = "width: 70%;object-fit: cover; height: 120px; float:left;" src = "{{ post.post_image }}">
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
					<img style = "width: 70%;object-fit: cover; height: 120px; float:right;" src = "{{ post.post_image }}">
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