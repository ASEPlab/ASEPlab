---
title: "Choi Lab - Team"
layout: gridlay
excerpt: "Choi Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

## Principal Investigator

<div class="team-section">
  {% for member in site.data.team %}
    {% if member.role == "PI" %}
      {% include team_member.html member=member %}
    {% endif %}
  {% endfor %}
</div>

## Group Members

**We are looking for new PhD students, Postdocs, and Master students to join the team!**

<div class="team-section">
  {% for member in site.data.team %}
    {% if member.role != "PI" %}
      {% include team_member.html member=member %}
    {% endif %}
  {% endfor %}
</div>

<style>
.team-section {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
</style>
