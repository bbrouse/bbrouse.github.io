---
layout: page
title: B(en's\s|rouse\s)?log
tagline: The ramblings of a nub software developer
---
{% include JB/setup %}

<div class="well well-large">
  <ul style="white-space:nowrap; overflow:hidden; list-style-type:none;">
    {% for post in site.posts limit 10 %}
    <li>
      <div>
        <div class="pull-left" style="width:85%;">
          <h2>
            <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a> - <span>{{ post.tagline }}</span>
          </h2>
        </div>
        <div class="pull-right">
          <h3>{{ post.date | date: "%B %e, %Y" }}</h3>
        </div>
      </div>
    </li>
    {% endfor %}
  </ul>
</div>
<hr>


