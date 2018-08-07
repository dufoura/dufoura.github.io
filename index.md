---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div id="home">
  <h1>Blog Posts</h1>
 
    {% for post in site.posts %}
    <div id="article"> 
    <div id="image"><img source="{{ site.baseurl }}/assets/Test.jpg"></div>
<div id="Bloc2">
    <div id="Titre"><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></div>

    <div id="Description">Description</div>
    <div id="Date">{{ post.date | date_to_string }}</div>
 </div>   
    
    </div>
    {% endfor %}
 
</div>
