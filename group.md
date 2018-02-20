---
layout: page
title: Research Group
---
{% include research_sub.html %}

![Group photo July 2017](./assets/photos/Group-201707.JPG)<br />
Corcovilos Lab members and alumni at the 2017 Undergraduate Research Symposium.
{: style="text-align: center; color: #606060; padding: 5px;
font-size: 0.9em; font-style: italic;"}

## Current members

### Faculty
{% for person in site.data.members %}
{% if person.current == "true" and person.type == "F" %}
* **{{ person.name }}** ({{ person.start }}--), {{ person.degree }} {{ person.grad }}
{% endif %}
{% endfor %}

### Undergraduate Students
{% for person in site.data.members %}
{% if person.current == "true" and person.type == "UG" %}
* **{{ person.name }}** ({{ person.start }}--), {{ person.degree }}, Graduating in {{ person.grad }}
{% endif %}
{% endfor %}

<!--
### High School Students
{% for person in site.data.members %}
{% if person.current == "true" and person.type == "HS" %}
* **{{ person.name }}** ({{ person.start }}--{{person.end}})
{% endif %}
{% endfor %}
-->

## Former members
### Undergraduate Students
{% for person in site.data.members %}
{% if person.current == "false" and person.type == "UG" %}
* **{{ person.name }}** ({{ person.start }}--{{person.end}}), {{ person.degree }}, {{ person. grad }}. {% if person.now %} Now: {{ person.now }}.{% endif %}
{% endif %}
{% endfor %}

### High School Students
{% for person in site.data.members %}
{% if person.current == "false" and person.type == "HS" %}
* **{{ person.name }}** ({{ person.start }}--{{person.end}}), {{ person.degree }}, {{ person. grad }}. {% if person.now %} Now: {{ person.now }}.{% endif %}
{% endif %}
{% endfor %}

## Current Collaborators
{% for person in site.data.members %}
{% if person.current == "true" and person.type == "C" %}
* **{{ person.name }}** {% if person.now %} {{ person.now }}.{% endif %}
{% endif %}
{% endfor %}
