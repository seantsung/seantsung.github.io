---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<div class="about-content">
<h2 id="about" class="section-heading">About Me</h2>

<p>Hi! I am Sean Tsung, a third-year PhD student in Management Science and Engineering at Stanford University, advised by Professors <a href="https://profiles.stanford.edu/margaret-brandeau">Margaret Brandeau</a> and <a href="https://www.gsb.stanford.edu/faculty-research/faculty/yue-hu">Yue Hu</a>.</p>

<p>My research sits at the intersection of healthcare operations, digital health, and health policy. I use operations research, causal inference, and AI methods to evaluate technology-enabled care and develop practical approaches that improve access, efficiency, and quality of care while helping health systems allocate scarce clinical capacity.</p>

<h2 id="education" class="section-heading">Education</h2>

<div class="education-section">
  <h3 class="pub-category-heading">Stanford University</h3>
  <p>
  Ph.D. in Management Science and Engineering (in progress)<br />
  M.S. in Epidemiology and Clinical Research (concurrent program, admitted 2025)</p>
  <ul class="education-subpoints">
    <li>Ph.D. Minor in Biomedical Data Science</li>
  </ul>

  <h3 class="pub-category-heading">University of California, Berkeley</h3>
  <p>
  M.S. in Industrial Engineering and Operations Research (awarded May 2023)<br />
  B.S. in Industrial Engineering and Operations Research (awarded May 2022)<br />
  B.A. in Data Science (awarded May 2022)</p>
  <ul class="education-subpoints">
    <li>Domain Emphasis in Linguistic Sciences</li>
  </ul>
</div>



<h2 id="publications" class="section-heading">Research Papers</h2>

{% if site.publication_category %}
  {% for category in site.publication_category %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
<h3 class="pub-category-heading">{{ category[1].title }}</h3>
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

<p class="cofirst-note"><em>* denotes co-first authorship.</em></p>

<h2 id="teaching" class="section-heading">Teaching</h2>
<h3 class="pub-category-heading">Teaching Assistant</h3>
<p>The Ethical Analyst<br /><i>Spring 2025, Spring 2026</i></p>
<p>Optimization and Simulation Modeling (MBA Core)<br /><i>Autumn 2025</i></p>
<p>Healthcare Operations Management<br /><i>Winter 2026</i></p>

</div>

