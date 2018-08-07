---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div id="home">
  <h1>Blog Posts</h1>
 
    {% for post in site.posts %}
    <div id="article">  <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a>
    {{ post.date | date_to_string }}
    Description
    </div>
    {% endfor %}
 
</div>
