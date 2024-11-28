---
permalink: /
title: "Academic Pages is a ready-to-fork GitHub Pages template for academic personal websites"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

This is the front page of a website that is powered by the [Academic Pages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages. [GitHub pages](https://pages.github.com) is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the repository. This template was forked from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) created by Michael Rose, and then extended to support the kinds of content that academics have: publications, talks, teaching, a portfolio, blog posts, and a dynamically-generated CV. You can fork [this template](https://github.com/academicpages/academicpages.github.io) right now, modify the configuration and markdown files, add your own PDFs and other content, and have your own site for free, with no ads!

About me
======
I am currently an Associate Professor at the School of Computer Science, Fudan University. Prior to joining Fudan, I was a Research Fellow at the School of Computing,  National University of Singapore (NUS), working with [Prof. Tat-Seng Chua](https://www.chuatatseng.com/). I received My Ph.D. degree in Computer Science from City University of Hong Kong in July 2018, supervised by [Prof. Chong-Wah Ngo](https://computing.smu.edu.sg/faculty/profile/601/ngo-chong-wah). I received several accolades, including the Best Student Paper Award at ACM Multimedia 2016, the Best Student Paper Award at Multimedia Modeling 2017, the"ACM Shanghai Rising Star Award" in 2020, and the "AI 2000 Most Influential Scholar Nomination Award" in 2021, “ACM SIGMM Rising Star Award” in 2024 and listed as “Stanford/Elsevier’s Top 2% Scientist” in 2024 etc.

Open Positions

------
I am looking for 2-3 interns working on Generative AI Security. Please fell free to email with your CV if you are intersted. 
Currently, there are no openings for PhD students starting in Fall 2025.

News

------

Selected Publications

<section id="selected-publications">
  <h2>Selected Publications</h2>
  <ul class="publications-list">
    {% for publication in site.publications %}
      {% if publication.selected %}
        <li class="publication-item">
          <div class="publication-content">
            <!-- 显示图片 -->
            {% if publication.image %}
              <div class="publication-image">
                <img src="{{ publication.image | relative_url }}" alt="{{ publication.title }}">
              </div>
            {% endif %}
            <!-- 显示标题、作者和日期 -->
            <div class="publication-details">
              <h3><a href="{{ publication.url | relative_url }}">{{ publication.title }}</a></h3>
              <p>
                <small>
                  {{ publication.date | date: "%B %Y" }}
                  {% if publication.authors %} - {{ publication.authors }}{% endif %}
                </small>
              </p>
            </div>
          </div>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
</section>


------
