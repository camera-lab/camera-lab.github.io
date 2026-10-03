---
title: "Publications"
layout: gridlay
excerpt: "Publications."
sitemap: true
permalink: /publications/
description:
nav: true
toc: true
---

Full publication list on [Google Scholar](https://scholar.google.com/citations?hl=en&user=CcSZwTsAAAAJ). Updated through 2026. Patents and duplicate preprint/published records are excluded.

<ul class="nav nav-tabs" style="width:100%; margin: 0 auto;">
    <li class="active">
    <a data-toggle="tab"><button id="btn_bytype" onclick="ShowOrHide('bytype')">By Type</button></a>
    </li>
    <li class="">
    <a data-toggle="tab"><button id="btn_byyear" onclick="ShowOrHide('byyear')">By Year</button> </a>
    </li>
    <li class="">
    <a data-toggle="tab"><button id="btn_inpress" onclick="ShowOrHide('inpress')">Preprint</button></a>
    </li>
</ul>

<br>

<script>var byyeartext="year";var bytypetext="type";</script>

{% assign publications = site.data.scholar_publications %}
{% assign year_groups = publications | group_by: "year" %}

{% capture publication_item %}{% endcapture %}

<div id="byyear" style="display:none;">
{% for group in year_groups %}
  <h3 id="{{ group.name | slugify }}">{{ group.name }}</h3>
  <ol class="bibliography">
  {% for paper in group.items %}
    <li><div id="{{ paper.id }}">
      <span class="author">{{ paper.authors }}</span>
      <a href="{{ paper.url }}" target="_blank" style="color:#555555;">“<span class="title"><u>{{ paper.title }}</u></span>,”</a>
      <span class="periodical"><em>{{ paper.venue }}</em></span>
      {% if paper.code != "" %}<a href="{{ paper.code }}" target="_blank" title="Code"><i class="fa fa-github fa-align-left fa-sm"></i></a>{% endif %}
    </div></li>
  {% endfor %}
  </ol>
{% endfor %}
</div>

<div id="inpress" style="display:none;">
## Preprints
{% assign preprints = publications | where: "type", "preprint" %}
<ol class="bibliography">
{% for paper in preprints %}
  <li><div id="preprint-{{ paper.id }}"><span class="author">{{ paper.authors }}</span> <a href="{{ paper.url }}" target="_blank" style="color:#555555;">“<span class="title"><u>{{ paper.title }}</u></span>,”</a> <span class="periodical"><em>{{ paper.venue }}</em></span>{% if paper.code != "" %} <a href="{{ paper.code }}" target="_blank" title="Code"><i class="fa fa-github fa-align-left fa-sm"></i></a>{% endif %}</div></li>
{% endfor %}
</ol>
</div>

<div id="bytype" style="display:block;">
## Journal papers
{% assign journal = publications | where: "type", "journal" %}
<ol class="bibliography">
{% for paper in journal %}
  <li><div id="journal-{{ paper.id }}"><span class="author">{{ paper.authors }}</span> <a href="{{ paper.url }}" target="_blank" style="color:#555555;">“<span class="title"><u>{{ paper.title }}</u></span>,”</a> <span class="periodical"><em>{{ paper.venue }}</em></span>{% if paper.code != "" %} <a href="{{ paper.code }}" target="_blank" title="Code"><i class="fa fa-github fa-align-left fa-sm"></i></a>{% endif %}</div></li>
{% endfor %}
</ol>

## Conference
{% assign conference = publications | where: "type", "conference" %}
<ol class="bibliography">
{% for paper in conference %}
  <li><div id="conference-{{ paper.id }}"><span class="author">{{ paper.authors }}</span> <a href="{{ paper.url }}" target="_blank" style="color:#555555;">“<span class="title"><u>{{ paper.title }}</u></span>,”</a> <span class="periodical"><em>{{ paper.venue }}</em></span>{% if paper.code != "" %} <a href="{{ paper.code }}" target="_blank" title="Code"><i class="fa fa-github fa-align-left fa-sm"></i></a>{% endif %}</div></li>
{% endfor %}
</ol>

## Books and Book Chapters
{% assign books = publications | where: "type", "book" %}
<ol class="bibliography">
{% for paper in books %}
  <li><div id="book-{{ paper.id }}"><span class="author">{{ paper.authors }}</span> <a href="{{ paper.url }}" target="_blank" style="color:#555555;">“<span class="title"><u>{{ paper.title }}</u></span>,”</a> <span class="periodical"><em>{{ paper.venue }}</em></span>{% if paper.code != "" %} <a href="{{ paper.code }}" target="_blank" title="Code"><i class="fa fa-github fa-align-left fa-sm"></i></a>{% endif %}</div></li>
{% endfor %}
</ol>

## Other Scholarly Works
{% assign other = publications | where: "type", "other" %}
<ol class="bibliography">
{% for paper in other %}
  <li><div id="other-{{ paper.id }}"><span class="author">{{ paper.authors }}</span> <a href="{{ paper.url }}" target="_blank" style="color:#555555;">“<span class="title"><u>{{ paper.title }}</u></span>,”</a> <span class="periodical"><em>{{ paper.venue }}</em></span>{% if paper.code != "" %} <a href="{{ paper.code }}" target="_blank" title="Code"><i class="fa fa-github fa-align-left fa-sm"></i></a>{% endif %}</div></li>
{% endfor %}
</ol>

</div>


<br><br>
