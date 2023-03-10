---
layout: default
meta-description: "LoG: Learning on Graphs and Geometry @ Oxford"
---

# LoG
The "Learning on Graphs and Geometry" reading group at Oxford University is a forum for discussing recent advances in the field of geometric deep learning, which lies at the intersection of machine learning and geometry. The group focuses on exploring the theoretical foundations and practical applications of graph neural networks, manifold learning, and other techniques for processing and analyzing data with a non-Euclidean structure. Members of the group include researchers and graduate students from various departments, including computer science, mathematics, and engineering, who share an interest in developing novel machine learning methods for understanding complex data sets with graph or geometric structure.




{% for category in site.data.talks %}
# {{ category.type }}
<div class="talk-list">
  {% for talk in category.members %}
  <div class="talk list-group-item">
  <div class="talk-date">{{ talk.date }}</div>
  <div class="talk-presenter">{{ talk.speaker }}</div>
  {% if talk.title %}
  <div>
    {% if talk.recording %}
      <span><a class="talk-title-link" href="{{ talk.recording }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
    {% elsif talk.livestream %}
      <span><a class="talk-title-link" href="{{ talk.livestream }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
    {% else %}
      <span>{{ talk.title }}</span>
      {% if talk.link %}
      <summary><a href="{{ talk.link }}">Link to paper</a> </summary>
      {% endif %}
      {% if talk.link2 %}
      <summary><a href="{{ talk.link2 }}">Link to second paper</a> </summary>
      {% endif %}
      {% if talk.link3 %}
      <summary><a href="{{ talk.link3 }}">Link to third paper</a> </summary>
      {% endif %}
    {% endif %}
  </div>
  {% endif %}
  {% if talk.abstract %}
    <details>
    <summary>Abstract</summary>
    {{ talk.abstract }}
    
    

    {% if talk.bio %}
    <br><br>
    <strong>Bio: </strong> {{ talk.bio }}
    {% endif %}

    {% if talk.recording %}
      <br><br>
      <strong><a href="{{ talk.recording }}">Video Link</a></strong>
    {% elsif talk.livestream %}
      <br><br>
      <strong><a href="{{ talk.livestream }}">Livestream Link</a></strong>
    {% endif %}
    </details>
  {% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}



