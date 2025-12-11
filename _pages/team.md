---
title: "Choi Lab - Team"
layout: gridlay
excerpt: "Choi Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

## Principal Investigator

{% assign pi = site.data.team_members | where: "role", "pi" | first %}

<div class="col-sm-12 col-md-6 col-lg-4 mb-4">
  <div class="card h-100">
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ pi.photo }}" class="card-img-top" alt="{{ pi.name }}">
    <div class="card-body">
      <h5 class="card-title">{{ pi.name }}</h5>
      <p class="card-text">
        {{ pi.info }}<br>
        email: <a href="mailto:{{ pi.email }}">{{ pi.email }}</a>
      </p>
      <ul>
        {% for i in (1..pi.number_educ) %}
          <li>{{ pi["education" | append: i] }}</li>
        {% endfor %}
      </ul>
    </div>
  </div>
</div>

---

## Group Members

**We are looking for new PhD students, Postdocs, and Master students to join the team!**

{% for member in site.data.team_members %}
  {% if member.role == "student" or member.role == "postdoc" %}

  <div class="col-sm-12 col-md-6 col-lg-4 mb-4">
    <div class="card h-100">
      <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="card-img-top" alt="{{ member.name }}">
      <div class="card-body">
        <h5 class="card-title">{{ member.name }}</h5>
        <p class="card-text">
          {{ member.info }}<br>
          email: <a href="mailto:{{ member.email }}">{{ member.email }}</a>
        </p>
        <ul>
          {% for i in (1..member.number_educ) %}
            <li>{{ member["education" | append: i] }}</li>
          {% endfor %}
        </ul>
      </div>
    </div>
  </div>

  {% endif %}
{% endfor %}
