---
title: Team
nav:
  order: 3
---

# Team

Our lab thrives on curiosity, teamwork, and a commitment to tackling key problems at the intersection of computational biology and environmental toxicology. Get to know the individuals driving our research forward!

{% include section.html %}
{% include list.html data="members" component="portrait" filter="role == 'pi'" %}
{% include list.html data="members" component="portrait" filter="role == 'phd'" %}
{% include list.html data="members" component="portrait" filter="role == 'postdoc'" %}
{% include list.html data="members" component="portrait" filter="role == 'intern'" %}
{% include list.html data="members" component="portrait" filter="role == 'new'" %}

## Alumni

<div class="table-wrapper" markdown="block">

{% assign alumni = site.members | where: "role", "alumni" | sort: "name" %}
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Role in Ewald Lab</th>
      <th>Future position</th>
    </tr>
  </thead>
  <tbody>
    {% for member in alumni %}
      <tr>
        <td><a href="{{ member.url | relative_url }}">{{ member.name }}</a></td>
        <td>{{ member.lab_role }}</td>
        <td>{{ member.future_position }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>

</div>
