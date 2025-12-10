---
title: "Choi Lab - Team"
layout: gridlay
excerpt: "Choi Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

**We are looking for new PhD students, Postdocs, and Master students to join the team!**

## Principal Investigator

{% assign first_member = site.data.team_members[0] %}
<div class="row">
  <div class="col-sm-12 clearfix">
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ first_member.photo }}" class="img-responsive" width="25%" style="float:left; margin-right: 20px;" />
    <h4>{{ first_member.name }}</h4>
    <i>{{ first_member.info }}</i>
    <ul style="overflow:hidden;">
      {% for i in (1..first_member.number_educ) %}
        {% assign educ_key = "education" | append: i %}
        <li>{{ first_member[educ_key] | markdownify }}</li>
      {% endfor %}
    </ul>
  </div>
</div>

<hr>

## Our Team

{% for member in site.data.team_members offset:1 %}
<div class="row">
  <div class="col-sm-12 clearfix">
    {% if member.photo != "" %}
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float:left; margin-right: 20px;" />
    {% endif %}
    <h4>{{ member.name }}</h4>
    <i>{{ member.info }}</i>
    <ul style="overflow:hidden;">
      {% for i in (1..member.number_educ) %}
        {% assign educ_key = "education" | append: i %}
        <li>{{ member[educ_key] | markdownify }}</li>
      {% endfor %}
    </ul>
  </div>
</div>
<br>
{% endfor %}
