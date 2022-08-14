---
layout: page
permalink: /teaching/
title: teaching
heading_title: Teaching
description: I have been teaching in the department of CSE, CUET for more than 3 years. Enjoyed teaching all the brilliant students of my department. So far, I have taught the following courses that are listed below.
nav: true
nav_order: 3
---
<div class="teaching">
<center>
<table>
  {% for row in site.data.courses %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
    {% if pair[1] == "Download" %}
    <center>
      <a href="{{row['Course Code'] | append: '.pdf' | prepend: 'assets/pdf/courses/' | relative_url}}" target="_blank" rel="noopener noreferrer">View</a>
    </center>
    {% else %}
      {{ pair[1] }}
    {% endif %}
    {% endtablerow %}
  {% endfor %}
</table>
</center>
<h3>Co-curricular</h3>
<hr>
<ul>
	<li style="text-align: justify;">
		<b style="color: var(--global-theme-color);">Competitive Programming Trainer: </b>I have been training competitive programming to the undergraduate students of my department and playing the role of a coach since I have joined as a faculty member. Along with some brilliant programmers, we preapred <a href="{{'assets/pdf/CUET CP Syllabus.pdf' | relative_url}}" target="_blank" rel="noopener noreferrer">this</a> syllabus to provide a proper guideline to the students.
	</li>
</ul>
</div>