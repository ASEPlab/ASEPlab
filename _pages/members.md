---
title: "Choi Lab - Members"
layout: gridlay
permalink: /members/
---
# Team Members

<div class="team-section">
  {% for member in site.data.team %}
    {% include team_member.html member=member %}
  {% endfor %}
</div>
