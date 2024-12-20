---
title: Team
permalink: /team/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|co|researchstaff|postdoc|phdstudent|gradstudent|visiting|others|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'co' %}
<h3>Co-PIs</h3>
 {% elsif role == 'pi' %}
<h3> Lead PI</h3>
 {% elsif role == 'researchstaff' %}
<h3>Research Staff</h3>
 {% elsif role == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
{% elsif role == 'phdstudent' %}
<h3>PhD Students</h3>
 {% elsif role == 'gradstudent' %}
<h3>Graduate Students</h3>
 {% elsif role == 'visiting' %}
<h3>Visiting Scholars</h3>
 {% elsif role == 'others' %}
<h3>Others</h3>
 {% elsif role == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ profile.new_url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ profile.new_url }}"><img class="profile-thumbnail" src="https://banffventureforum.com/wp-content/uploads/2019/08/no-photo-icon-22.png"></a>
          {% endif %}
          <a class="name" href="{{ profile.new_url }}">{{ profile.name }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}

<br>

| Who are they | When were they here | Where they went |
| :------------- |:-------------| :-----------|
| [Tony Liu](https://tliutony.github.io/) | Graduate Student (2018-2024) | Assistant Professor of Computer Science, Mount Holyoke College |
{% endif %}
{% endfor %}
