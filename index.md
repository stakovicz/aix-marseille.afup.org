---
layout: page
active: archive
has_left_logo: true
---

  <style>
  .read-more {
  display:inline-block;
  padding: 10px 30px;
  background-color:#ed0678;
  color:#fff;
  font-size: 130%;
  text-transform: capitalize;
  text-decoration: none;
  font-family: Arimo, "Helvetica Neue", Helvetica, Arial, sans-serif;
  }
  </style>

  <h2 class="category-key">Dernier article</h2>

  <ul class="year">
    {% for post in site.posts %}
        <li>
            <a href="{{ post.url | relative_url}}"
            {% if forloop.first %} style="font-weight:bold" {%endif %}
            >{{ post.title }}</a>
            <span class="date">{{ post.date | date: "%d/%m/%Y"  }}</span>
            
          {% if forloop.first %}
            {{ post.excerpt }}
            
            <div style="text-align:right">
<a href="{{ post.url | relative_url}}" class="read-more">VOIR PLUS</a>
            </div>
            </li>
            </ul>
<h2 class="category-key">Articles précédents</h2>
<ul class="year">
            
            {% else %}
            </li>          
          {% endif %}
        
    {% endfor %}
  </ul>

