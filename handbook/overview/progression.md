---
title: Progression
ladders:
    - type: Individual Contributor
      roles:
        - Engineer I
        - Engineer II
        - Senior Engineer I
        - Senior Engineer II
        - Staff Engineer I
        - Staff Engineer II
        - Principal Engineer I
        - Principal Engineer II
    - type: Management
      roles:
        - Lead
        - Manager
        - Senior Manager
---
Enhancing your craft and getting better as an engineer is of critical importance to the team. **Stagnation is not allowed**. Your effort and improvements will be recognized and rewarded.

At Pangea, we recognize that Engineering progression has two routes: **Individual Contributor** or **Management**. However, you must be a Senior Individual Contributor before you can transition into the Management route.

Progression is measured as improvements in the following areas:

- Technical Skills
- Task Management
- Communication
- Architecture

## Ladders

{% assign ladders = page.ladders | group_by: 'type' %}

{% for ladder in ladders %}

### {{ ladder.name }}
{% assign roles = ladder.items | first %}
{% for role in roles.roles %}
- {{ role }}
{% endfor %}
{% endfor %}