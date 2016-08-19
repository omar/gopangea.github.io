---
layout: page
permalink: /join/index.html
title: Join
---

### Who we are

Founded in 2012 and headquartered in Chicago, IL, Pangea started with the mission of making money transfer simple, fair and safe. Since then, we’ve been striving to enhance the security and reduce the cost and pain points of international money transfer.

Our first solution allows users to complete a transfer in three easy steps and pay with any US debit card, with an innovative nationwide cash solution coming soon. Receivers in Mexico, Colombia, Guatemala, El Salvador and Dominican Republic can collect the transfers in cash or receive the money directly into a bank account. Through every partnership and product iteration, we’ll continue to help our users save more time and money.  

Pangea is successful because of our world-class team members and strong passion for making an impact in our customers’ lives. We are different. We are innovative. We are eager to learn from each other. We are dedicated to building the world’s best platform for transferring money.

### Openings

{% assign teams = site.jobs | group_by: "team" %}

{% for team in teams %}
  <h4>{{ team.name }}</h4>
  
  <ul>
    {% for job in team.items %}
    <li><a href="{{ job.url }}">{{ job.title }}</a></li>
    {%endfor%}
  </ul>

{% endfor %}