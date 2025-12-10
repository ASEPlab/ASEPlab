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
    <img src="{{ site.baseurl }}/images/teampic/{{ first_member.photo }}" class="img-responsive" width="25%" style="float:left;" />
    <h4>{{ first_member.name }}</h4>
    <i>{{ first_member.info }}</i>
    <ul style="overflow:hidden;">
      {% for i in (1..first_member.number_educ) %}
        <li>{{ first_member["education" | append:i] | markdownify }}</li>
      {% endfor %}
    </ul>
  </div>
</div>

## Our Group Members

{% assign remaining_members = site.data.team_members | slice: 1, site.data.team_members.size %}
{% for member in remaining_members %}
<div class="row">
  <div class="col-sm-12 clearfix">
    <img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float:left;" />
    <h4>{{ member.name }}</h4>
    <i>{{ member.info }}</i>
    <ul style="overflow:hidden;">
      {% for i in (1..member.number_educ) %}
        <li>{{ member["education" | append:i] | markdownify }}</li>
      {% endfor %}
    </ul>
  </div>
</div>
{% endfor %}
