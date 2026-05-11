## 学位

- 修士（文学）（千葉大学、2022年3月）（学位論文：理解の内在主義に対する批判的検討）
- 学士（文学）（龍谷大学、2020年3月）（学位論文：経験的知識の確実性について）

## 職歴

<ul>
  {% for experience in site.data.cv.experience %}
  <li>{{ experience.institution }}、{{ experience.position }}（{{ experience.duration }}）</li>
  {% endfor %}
</ul>

## 学歴

<ul>
  {% for education in site.data.cv.education %}
  <li>{{ education.institution }}（{{ education.duration }}）</li>
  {% endfor %}
</ul>

## 論文

<ul>
  {% for publication in site.data.outputs.publications %}
  <li>
    {{ publication.title }} [<a href="{{ publication.url }}">刊行版へのアクセス</a>]<br />
    {% if publication.type == "incollection" %}
    {{ publication.booktitle }}（{{ publication.series }}、第{{ publication.number }}号）、{{ publication.year }}年
    {% elsif publication.type == "article" %}
    {{ publication.journal }}、第{{ publication.number }}号、{{ publication.year }}年
    {% endif %}
  </li>
  {% endfor %}
</ul>

## 口頭発表

<ul>
  {% for presentation in site.data.outputs.presentations %}
  <li>
    {{ presentation.title }}
    {% for link in presentation.links %}
    [<a href="{{ link.url }}">{{ link.label }}</a>]
    {% endfor %}<br />
    {{ presentation.conference }}（{{ presentation.venue }}）、{{ presentation.date }}
  </li>
  {% endfor %}
</ul>

## 担当経験のある科目

<ul>
  {% for course in site.data.cv.courses %}
  <li>{{ course.title }}（{{ course.institution }}）</li>
  {% endfor %}
</ul>

## 所属学会

- 日本科学哲学会
- 応用哲学会

---

- [GitHub](https://github.com/sotanigawa)
- [Google Scholar](https://scholar.google.co.jp/citations?user=o9_vcfoAAAAJ)
- [Academia.edu](https://chiba-u.academia.edu/SotaroTanigawa)
