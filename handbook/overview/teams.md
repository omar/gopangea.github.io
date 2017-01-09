---
title: Teams
---
{% assign teams = site.data.team | group_by:'team' %}
{% for team in teams %}
<div class="team">
    <h2>{{ team.name }} ({{ team.items | size }})</h2>
    <ul class="team-members">
        {% for member in team.items %}
        <li>
            {% if member.avatar %}
            <img class="photo" src="{{ member.avatar }}" />
            {% else %}
            <img class="photo" src="/assets/avatar-placeholder.png" />
            {% endif %}
            <span class="name">{{ member.name }}</span>
            <span class="role">{{ member.role }}</span>
            <div class="social">
            {% if member.social.github %}
                <a href="{{ member.social.github }}"><i class="fa fa-github fa-lg">&nbsp;</i></a>
            {% endif %}
            {% if member.social.stackoverflow %}
                <a href="{{ member.social.stackoverflow }}"><i class="fa fa-stack-overflow fa-lg">&nbsp;</i></a>
            {% endif %}
            {% if member.social.linkedin %}
                <a href="{{ member.social.linkedin }}"><i class="fa fa-linkedin fa-lg">&nbsp;</i></a>
            {% endif %}
            {% if member.social.twitter %}
                <a href="{{ member.social.twitter }}"><i class="fa fa-twitter fa-lg">&nbsp;</i></a>
            {% endif %}
            </div>
        </li>
        {% endfor %}
    </ul>
</div>
{% endfor %}

