---
title: "Alpha-VLLM team - Works"
layout: gridlay
excerpt: "Alpha-VLLM team -- Works."
sitemap: false
permalink: /works/
---


# Works

For all publications of our laboratory, we follow the convention of indicating all co-first authors by bolding their names in the authorship listing. Additionally, the corresponding authors will be noted with a dagger symbol (†). 

**At the end of this page, you can find the [full list of publications and projects](#All-Publication-by-year).**

## Reseach Area
- Multimodal Large Language Models, 
- Generative Agents
- Diffusion Models

## Project Highlights 

{% assign number_printed = 0 %}
{% for publi in site.data.project %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/propic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

## All Research Projects  ![Star](https://img.shields.io/badge/Overall_Stars-10k+-blue?style=social&logo=github)

{% for publi in site.data.project %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

## All Publication by year

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}








