---
title: Test of Time Awards
order: 5
---

In 2018, the ESEC/FSE [steering committee]({% link pages/steering_committee.md %}) has installed a Test of Time Award. The Test of Time Award is given annually recognizing highly influential papers published ten years ago in ESEC or FSE.

{% assign award_years = site.data.test_of_time_awards | sort: "year" | reverse %}
{% for award_year in award_years %}
## {{ award_year.year}}  <small><small>(selected from {{ award_year.conference_published }})</small></small>
{% if award_year.awardees.size > 1 %}
#### Award Papers:
{% else %}
#### Award Paper:
{% endif %}
{% for award_paper in award_year.awardees %}
[{{ award_paper.title }}]({{award_paper.link}})<br>
<small>{{ award_paper.authors }}</small>
{% endfor %}

{% if award_year.honorable_mentions.size > 0 %}
{% if award_year.honorable_mentions.size > 1 %}
#### Honorable Mentions:
{% else %}
#### Honorable Mention:
{% endif %}
{% for honorable_mention in award_year.honorable_mentions %}
[{{ honorable_mention.title }}]({{honorable_mention.link}})<br>
<small>{{ honorable_mention.authors }}</small>
{% endfor %}
{% endif %}

#### Selection Committee:
<small>{{ award_year.committee }}</small>
{% endfor %}

