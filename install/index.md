---
layout: page
title: Install Animation
project: Install Animation
aside: Fun with SVGs and animation
img: /img/svg/splash-inst.svg
class: install
type: project
---

## Showing up

Testing here

<div markup="0" class="wide codepen">
    <p data-height="734" data-theme-id="light" data-slug-hash="WxrKPj" data-default-tab="result" data-user="zherring" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/zherring/pen/WxrKPj/">install screen v2</a> by Zach Herring (<a href="http://codepen.io/zherring">@zherring</a>) on <a href="http://codepen.io">CodePen</a>.</p>
    <script async src="//assets.codepen.io/assets/embed/ei.js"></script>
</div>

<div>
{% if page.previous.url %}
    <a class="prev" href="{{page.previous.url}}">&laquo; {{page.previous.title}}</a>
  {% endif %}
  {% if page.next.url %}
    <a class="next" href="{{page.next.url}}">{{page.next.title}} &raquo;</a>
  {% endif %}
</div>



<!-- {% for page in site.pages %}

{% if page.type == "project" %}

<a markdown="0" class="splash {{ page.class }}" href="{{ site.baseurl }}{{ page.url }}">
<img markdown="0"  src=" {{ page.img }}" />
<h2 markdown="0" > {{ page.title }} </h2>
<aside markdown="0" > {{ page.aside }} </aside>
</a>
{% endif%}

{% endfor %} -->
