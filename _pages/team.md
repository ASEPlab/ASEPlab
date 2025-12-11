---
title: "Choi Lab - Team"
layout: gridlay
excerpt: "Group Members"
sitemap: false
permalink: /team/
---

# Our Team

## Principal Investigator

{% assign pi = site.data.team_members | where: "role", "pi" | first %}

<div class="row">
  <div class="col-sm-12 clearfix">
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ pi.photo }}" class="img-responsive" width="20%" style="float: left; margin-right: 20px;" />
    <h4>{{ pi.name }}</h4>
    <i>{{ pi.info }}<br>email: {{ pi.email }}</i>
    <ul style="overflow: hidden">
      {% for i in (1..pi.number_educ) %}
        <li>{{ pi["education" | append: i] }}</li>
      {% endfor %}
    </ul>
  </div>
</div>

---

## Group Members

**We are looking for new PhD students, Postdocs, and Master students to join the team!**

<div class="row">

{% for member in site.data.team_members %}
  {% if member.role == "student" or member.role == "postdoc" %}

  <div class="col-sm-12 clearfix" style="margin-bottom: 30px;">
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="20%" style="float: left; margin-right: 20px;" />
    <h4>{{ member.name }}</h4>
    <i>{{ member.info }}<br>email: {{ member.email }}</i>
    <ul style="overflow: hidden">
      {% for i in (1..member.number_educ) %}
        <li>{{ member["education" | append: i] }}</li>
      {% endfor %}
    </ul>
  </div>

  {% endif %}
{% endfor %}

</div>
