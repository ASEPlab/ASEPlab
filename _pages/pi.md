---
title: "Choi Lab - PI"
layout: gridlay
permalink: /pi/
---
# Principal Investigator

<div class="team-section">
  {% for member in site.data.team %}
    {% if member.role == "pi" %}
      {% include team_member.html member=member %}
    {% endif %}
  {% endfor %}
</div>
