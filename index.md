---
layout: default
---

  {% for post in paginator.posts %}
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
  {% endfor %}

  <div class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_url }}">Previous</a>
    {% endif %}
    Page {{ paginator.page }} of {{ paginator.total_pages }}
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_url }}">Next</a>
    {% endif %}
  </div>