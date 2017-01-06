---
layout: base
title: Pangea Engineering
---

<div class="col-left">
    <div class="content">
        <h2>Posts</h2>

        <ul class="post-list">
            {% for post in site.posts %}
            <li>
                <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }} {% if post.author %} by {{ site.data.team[post.author].name }}{% endif %}</span>
                <h2>
                <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
                </h2>
            </li>
            {% endfor %}
        </ul>
    </div>
</div>

<div class="col-right">
    <div class="content">
        <h2>About</h2> 
        <p>
        This blog is operated by the <a href="https://gopangea.com">Pangea</a> engineering team.
        </p>

        <p>
        We'll use this blog to showcase our work and inform others of our solutions to the problems we face.
        </p>

        <p>You can find our open source work at <a href="https://github.com/gopangea">github.com/gopangea</a>.</p>
    </div>
</div>