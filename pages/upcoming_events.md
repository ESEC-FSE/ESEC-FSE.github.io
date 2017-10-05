---
title: Upcoming Events
order: 2
---
{% assign event_categories = site.data.events_upcoming | group_by: "category" %}
{% for event_category in event_categories %}
## Upcoming instances of {{ event_category.name }}

{% assign events = event_category.items | sort: "year" | reverse %}
{% for event in events -%}
* {% if event.link != nil %}[{{ event.name }}]({{ event.link }}){% else %}{{ event.name }}{% endif %}  
  {{ event.location }}, {{ event.year }}
{% endfor %}
{% endfor %}
