---
layout: default
title: Athos World|我的生活
whereami: index
---

#### 你好

这里都是我的故事


---

#### 文章列表:

<div class="post-list-body">
    <div post-cate="All">
        <ul>
            {% for post in site.posts %}
            <li>{{ post.date | date:"%Y-%m-%d" }} <a href="{{ post.url }}"> {{ post.title }}</a></li>
            {% endfor %}
        </ul>
    </div>
    {% for tag in site.tags %}
      <div post-cate="{{tag | first}}">
        <ul>
        {% for posts in tag  %}
          {% for post in posts %}
            {% if post.url %}
              <li>{{ post.date | date:"%Y-%m-%d" }} <a href="{{ post.url }}"> {{ post.title }}</a></li>
            {% endif %}
          {% endfor %}
        {% endfor %}
        </ul>
      </div>
    {% endfor %}
</div>
