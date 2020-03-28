---
layout: page
title: Research
permalink: /projects/
description: My current research interests can be grouped in the following topics.
---

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h7 class="author">{{ project.description }}</h7>
            <h1>{{ project.title }}</h1>
        </span>
        </a>
    </div>
</div>

{% else %}

{% if project.selfdirect %}
<div class="project ">
    <div class="thumbnail">
        <a href="{{ '/projects/' | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h7 class="author">{{ project.description }}</h7>
            <h1>{{ project.title }}</h1>
        </span>
        </a>
    </div>
</div>

{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h7 class="author">{{ project.description }}</h7>
            <h1>{{ project.title }}</h1>
        </span>
        </a>
    </div>
</div>
{% endif %}

{% endif %}

{% endfor %}
