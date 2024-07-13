Sotaro Tanigawa is a PhD student at Chiba University, working mainly in epistemology, a branch of philosophy.

\[[GitHub](https://github.com/sotanigawa)\]
\[[Google Scholar](https://scholar.google.co.jp/citations?user=o9_vcfoAAAAJ)\]
\[[Academia.edu](https://chiba-u.academia.edu/SotaroTanigawa)\]

### Publications (mostly in Japanese)

<ul>
{% for p in site.data.achievements.publications %}
  <li>
    <strong>{{ p.title }}</strong>
    {% for url in p.urls %}
    [<a href="{{ url[1] }}">{{ url[0] }}</a>]
    {% endfor %}
    <br />
    <i>{{ p.journal }}</i>, Number {{ p.number }}, {{ p.year }}
  </li>
{% endfor %}
</ul>

### Talks (mostly in Japanese)

<ul>
{% for t in site.data.achievements.talks %}
  <li>
    <strong>{{ t.title }}</strong>
    {% for url in t.urls %}
    [<a href="{{ url[1] }}">{{ url[0] }}</a>]
    {% endfor %}
    <br />
    <i>{{ t.conference }}</i>, {{ t.venue }}, {{ t.dates }}
  </li>
{% endfor %}
</ul>

### Education

<ul>
{% for e in site.data.education %}
  <li>
    <strong>{{ e.institution }}</strong>, {{ e.during }}{% if e.degree %}<br />
    <i>{{ e.degree }}</i>{% endif %}{% if e.thesis %}, Thesis: {{ e.thesis }}{% endif %}
  </li>
{% endfor %}
</ul>

### Professional Experience

<ul>
{% for p in site.data.experience.professional %}
  <li><strong>{{ p.position }}</strong>, {{ p.institution }}, {{ p.duration }}</li>
{% endfor %}
</ul>

### Teaching Experience

<ul>
{% for t in site.data.experience.teaching %}
  <li><strong>{{ t.position }}</strong>, <i>{{ t.course_title }}</i>, {{ t.institution }}, {{ t.term }}</li>
{% endfor %}
{% for t in site.data.experience.tutoring %}
  <li><strong>{{ t.position }}</strong>, {{ t.institution }}, {{ t.duration }}</li>
{% endfor %}
</ul>
