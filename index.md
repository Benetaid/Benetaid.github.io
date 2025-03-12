---
layout: default  
title : Home
---

# 欢迎来到我的个人网站!

我是沙花，希望能和你有一次愉快的交流。՞˶･֊･˶՞ 


<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
    </li>
  {% endfor %}
</ul>

{% if site.paginator.total_pages > 1 %}
  <ul class="pagination">
    {% if site.paginator.previous_page %}
      <li><a href="{{ site.paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">Previous</a></li>
    {% endif %}
    {% if site.paginator.next_page %}
      <li><a href="{{ site.paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Next</a></li>
    {% endif %}
  </ul>
{% endif %}
