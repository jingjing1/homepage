---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am currently an Associate Professor at the School of Computer Science, Fudan University. Prior to joining Fudan, I was a Research Fellow at the School of Computing,  National University of Singapore (NUS), working with [Prof. Tat-Seng Chua](https://www.chuatatseng.com/). I received My Ph.D. degree in Computer Science from City University of Hong Kong in July 2018, supervised by [Prof. Chong-Wah Ngo](https://computing.smu.edu.sg/faculty/profile/601/ngo-chong-wah). I received several accolades, including the Best Student Paper Award at ACM Multimedia 2016, the Best Student Paper Award at Multimedia Modeling 2017, the"ACM Shanghai Rising Star Award" in 2020, and the "AI 2000 Most Influential Scholar Nomination Award" in 2021, “ACM SIGMM Rising Star Award” in 2024 and listed as “Stanford/Elsevier’s Top 2% Scientist” in 2024 etc.

------

### Open Positions

* I am looking for 2-3 interns working on Generative AI Security. Please fell free to email with your CV if you are intersted. 
* Currently, there are no openings for PhD students starting in Fall 2025.

### News

[Nov 2024] My Ph.D. student, Weizhi Peng (graduated in June 2024), has been awarded the CSIG Outstanding Doctoral Dissertation Award!

------


### Selected Publications

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      <!-- 显示图片 -->
      {% if publication.image %}
        <div class="publication-image">
          <img src="{{ publication.image | relative_url }}" alt="{{ publication.title }}">
        </div>
      {% endif %}
       <!-- 显示标题、作者和日期 -->
      {% unless title_shown %}
        <p>{{ category[1].title }}</p><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}


