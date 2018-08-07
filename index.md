---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div id="home">
  <h1>Blog Posts</h1>
 
    {% for post in site.posts %}
    <div id="article"> 
    <div class="Image">Image</div>

    <div class="Titre"><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></div>

    <div class="Description">Description</div>
    <div class="date">{{ post.date | date_to_string }}</div>
    
    
    </div>
    {% endfor %}
 
</div>
