---
layout: main
title : Blog
header : Blog
group: navigation
---


 <section class="container">
        
        <header>
            <h3>Recent posts</h3>
        </header>
        
        <ul class="posts">
            {% for post in site.posts offset: 0 limit: 6 %}
            <li>
            <span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ base.url }}{{ post.url }}">{{ post.title }}</a><br/>
            <!-- {{ post.excerpt | strip_html | truncatewords:75 }} -->
            </li>
            {% endfor %}
        </ul>


    </section>

 <section class="container">
        

        <header >
            <h3>All posts</h3>
        </header>
        
        <ul class="posts">
        {% for post in site.posts offset: 6 %}
            <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ base.url }}{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
        </ul>        
    
</section>
