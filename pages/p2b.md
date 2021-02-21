---
layout: kz-page
title: Plastic 2 Build
permalink: /p2b/
header: no
image:
    title: p2b_banner.jpg
widgets:
- url: 
  image: p2b_1.jpg
  cols: 4
- url: 
  image: p2b_2.jpg
  cols: 4
- url: 
  image: p2b_3.jpg
  cols: 4

---

Some text here...


<div class="row">
  {% for widget in page.widgets %}
    {% assign loopindex = forloop.index | modulo: 3 %}
    <div id="{{ widget.anchor }}">{% include _frontpage-widget.html widget=widget %}</div>
    {% if loopindex == 0 %}
  <hr style="height:1px; visibility:hidden;" /> <!-- Prevents long first column items from pushing new rows to the right -->
    {% endif %}
  {% endfor %}
</div>


Some more text here...