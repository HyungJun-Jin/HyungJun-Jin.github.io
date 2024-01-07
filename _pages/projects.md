---
# layout: archive
title: "Projects"
permalink: /projects/
classes: wide
author_profile: true
---


<!-- <iframe src="https://mlnotebook.github.io/img/CNN/convSobel.gif" width="640" height="480"></iframe>{: .align-right}

<img src="https://mlnotebook.github.io/img/CNN/convSobel.gif" width="50" height="50">{: .align-center}

![image-center](/images/profile/profile_img.png){:.align-center} -->

{% if post.id %}
  {% assign title = post.title | markdownify | remove: "<p>" | remove: "</p>" %}
{% else %}
  {% assign title = post.title %}
{% endif %}


{% for post in site.projects reversed -%}
  {% assign i = forloop.index0 | modulo: 2 %}
  {% if i == 0 %}
  <p>
  <img src="https://mlnotebook.github.io/img/CNN/convSobel.gif" width="100" height="100" />
  </p>{: .align-right}
  <h2 class="archive__item-title-v2" itemprop="headline">
      {% if post.link and post.collection != 'publications' %}
      <a href="{{ post.link }}">{{ title }}</a> <a href="{{ base_path }}{{ post.url }}" rel="permalink"><i class="fa fa-link" aria-hidden="true" title="permalink"></i><span class="sr-only">Permalink</span></a>
      {% else %}
      <a href="{{ base_path }}{{ post.url }}" rel="permalink">{{ title }}</a>
      {% endif %}
  </h2>

  ## Abstract 
  In this project we developed a deep learning based server using Flask. This server can be used from anywhere around the globe. All you have to do is just uplaod the image of a plant and it will through our servers and your will see the output as shown in video (all diseases highlighted).
  {: .align-right}

  {% else %}
  {{ i }}
  {% endif %}
  <br>
{% endfor %}


<!--
{% for post in site.projects reversed -%}
  {% if forloop.index0 | modulo: 2 %}
    {% include archive-thumbnail.html %}
  {% else %}
    {% continue %}
  {% endif %}
{% endfor %}


<!-- html
{% for post in site.projects reversed %}
  {% include archive-thumbnail.html %}
{% endfor %} 

{{ forloop.index0 | modulo: 2 }}

-->

