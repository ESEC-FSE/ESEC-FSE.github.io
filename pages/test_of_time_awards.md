---
title: Test of Time Awards
order: 5
---

In 2018, the ESEC/FSE [steering committee]({% link pages/steering_committee.md %}) has installed a Test of Time Award. The Test of Time Award is given annually recognizing highly influential papers published ten years ago in ESEC or FSE.

{% assign award_years = site.data.test_of_time_awards | sort: "year" %}
{% for award_year in award_years %}
## {{ award_year.year}}  <small><small>(selected from {{ award_year.conference_published }})</small></small>
#### Award Papers:
{% for award_paper in award_year.awardees %}
[{{ award_paper.title }}]({{award_paper.link}})<br>
<small>{{ award_paper.authors }}</small>
{% endfor %}
#### Selection Committee:
<small>{{ award_year.committee }}</small>
{% endfor %}
