---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div id="home">
  <h1>Les dernières actus</h1>
 
    {% for post in site.posts %}
    <div id="article"> 
    <div id="image"><img height="150" width="150" src="{{ "/assets/img/" | absolute_url }}{{post.image}}"></div>
<div id="Bloc2">
    <div id="Titre"><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></div>

    <div id="Description">{{post.resume}}</div>
    <div id="Date">{{ post.date | date_to_string }}</div>
 </div>   
    
    </div>
    {% endfor %}
 
</div>
