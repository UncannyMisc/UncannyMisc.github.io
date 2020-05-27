---
is_main: True
---
### Articles

This page will index article pages I post.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site uses the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/UncannyMisc/UncannyMisc.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

<div style = "width: -webkit-fill-available;">
  {% assign startrow = true %}
  {% for post in site.posts %}
    <div style = "width = 100%; float:left;">
		{% if startrow == true%}
			<div style = "width: 70%; float:left;" href="{{ post.url }}" title = "{{ post.title }}">
				<img style = "object-fit: cover; width: 100%; height: 100px;" src = "{{ post.post_image }}">
			</div>
			{% assign startrow = false %}
		{% else %}
			<div style = "width: 70%; float:right;" href="{{ post.url }}" title = "{{ post.title }}">
				<img style = "object-fit: cover; width: 100%; height: 100px;" src = "{{ post.post_image }}">
			</div>
			{% assign startrow = true %}
		{% endif %}
    </div>
  {% endfor %}
</div>