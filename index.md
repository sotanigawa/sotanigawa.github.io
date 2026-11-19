---
title: アカデミック・ポートフォリオ
description: 谷川綜太郎（Sotaro Tanigawa）のアカデミック・ポートフォリオ
---

## 論文

{% assign publications = site.data.publications | sort: "year" | reverse %}
<ul>
  {% for publication in publications %}
  <li>
    {{ publication.title }}
    {% for link in publication.links %}
    [<a href="{{ link.url }}">{{ link.label }}</a>]
    {% endfor %}<br />
    {% if publication.type == "incollection" %}
    {{ publication.booktitle }}（{{ publication.series }}、第{{ publication.number }}号）、{{ publication.year }}年
    {% elsif publication.type == "article" %}
    {{ publication.journal }}、第{{ publication.number }}号、{{ publication.year }}年
    {% endif %}
  </li>
  {% endfor %}
</ul>

## 口頭発表

{% assign presentations = site.data.presentations | sort: "date" | reverse %}
<ul>
  {% for presentation in presentations %}
  <li>
    {{ presentation.title }}
    {% for link in presentation.links %}
    [<a href="{{ link.url }}">{{ link.label }}</a>]
    {% endfor %}<br />
    {{ presentation.conference }}（{{ presentation.venue }}）、{{ presentation.date | date: "%Y年%-m月%-d日" }}
  </li>
  {% endfor %}
</ul>

## 職歴

{% assign positions = site.data.positions | sort: "start_year" | reverse %}
<ul>
  {% for position in positions %}
  {% capture period %}
    {%- if position.end_year == nil -%}
      {{ position.start_year }}年度–現在
    {%- elsif position.end_year == position.start_year -%}
      {{ position.start_year }}年度
    {%- else -%}
      {{ position.start_year }}–{{ position.end_year }}年度
    {%- endif -%}
    {%- if position.note -%}・{{ position.note }}{%- endif -%}
  {% endcapture %}
  <li>{{ position.institution }}、{{ position.position }}（{{ period | strip }}）</li>
  {% endfor %}
</ul>

## 学歴

{% assign education = site.data.education | sort: "start" | reverse %}
<ul>
  {% for entry in education %}
  {% assign start_ym = entry.start | split: "-" %}
  {% capture period %}
    {{- start_ym[0] }}年{{ start_ym[1] | plus: 0 }}月–
    {%- if entry.end -%}
      {%- assign end_ym = entry.end | split: "-" -%}
      {{ end_ym[0] }}年{{ end_ym[1] | plus: 0 }}月
    {%- else -%}
      現在
    {%- endif -%}
  {% endcapture %}
  <li>{{ entry.institution }}（{{ period | strip }}）</li>
  {% endfor %}
</ul>

## 学位

{% assign degrees = site.data.degrees | sort: "date" | reverse %}
<ul>
  {% for degree in degrees %}
  {% assign date_ym = degree.date | split: "-" %}
  <li>{{ degree.degree }}（{{ degree.institution }}、{{ date_ym[0] }}年{{ date_ym[1] | plus: 0 }}月）（学位論文：{{ degree.thesis }}）</li>
  {% endfor %}
</ul>

## 担当経験のある科目

<ul>
  {% for course in site.data.courses %}
  <li>{{ course.title }}（{{ course.institution }}）</li>
  {% endfor %}
</ul>

## 所属学会

<ul>
  {% for society in site.data.societies %}
  <li>{{ society.name }}</li>
  {% endfor %}
</ul>

---

- [GitHub](https://github.com/sotanigawa)
- [Google Scholar](https://scholar.google.co.jp/citations?user=o9_vcfoAAAAJ)
- [Academia.edu](https://chiba-u.academia.edu/SotaroTanigawa)
