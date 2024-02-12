Sotaro Tanigawa is a PhD student at Chiba University, working mainly in epistemology, a branch of philosophy. The following topics are the current focus of his research:

- The nature and value of knowledge, understanding, and wisdom
- Value problems, the swamping problem, and epistemic value monism/pluralism
- The relation between curiosity, inquiry, and epistemic goals

He is also interested in empirical theories of learning in psychology and data science, as well as experimental approaches in philosophy.

\[[GitHub](https://github.com/sotanigawa)\]
\[[Google Scholar](https://scholar.google.co.jp/citations?user=o9_vcfoAAAAJ)\]
\[[Academia.edu](https://chiba-u.academia.edu/SotaroTanigawa)\]

### Publications (mostly in Japanese)

<ul>
{% for p in site.data.achievements.publications %}
  <li>
    <strong>{{ p.title }}</strong><br />
    <i>{{ p.journal }}</i>, Number {{ p.number }}, {{ p.year }}<br />
    {% for url in p.urls %}
    [<a href="{{ url[1] }}">{{ url[0] }}</a>]
    {% endfor %}
  </li>
{% endfor %}
</ul>

### Talks (mostly in Japanese)

<ul>
{% for t in site.data.achievements.talks %}
  <li>
    <strong>{{ t.title }}</strong><br />
    <i>{{ t.conference }}</i>, {{ t.venue }}, {{ t.dates }}<br />
    {% for url in t.urls %}
    [<a href="{{ url[1] }}">{{ url[0] }}</a>]
    {% endfor %}
  </li>
{% endfor %}
</ul>

### Education

- **Graduate School of Humanities and Studies on Public Affairs, Chiba University**, April 2022 &ndash; Present  
  _PhD Student in Philosophy_
- **Graduate School of Humanities and Studies on Public Affairs, Chiba University**, April 2020 &ndash; March 2022  
  _MA in Philosophy_
  - Thesis: “A Critical Study of Internalism About Understanding”
- **Faculty of Letters, Ryukoku University**, April 2016 &ndash; March 2020  
  _BA in Philosophy_
  - Thesis: “On the Certainty of Empirical Knowledge”
- **Aiko Junior/Senior High School**, April 2009 &ndash; March 2015

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
