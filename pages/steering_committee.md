---
title: Steering Committee
order: 4
---
The FSE Steering Committee is responsible for constituting and guiding each edition of FSE and for establishing and evaluating practices that are binding upon the organizers of each conference for the continued technical and financial success of the conference.

In particular, the FSE Steering Committee is the body that is responsible for long term policies of the FSE conference series. 

The tasks of the steering committee are the following:

* Defining the scope, aims, and long-term evolution of the conference series
* Establishing the rules governing choice of officers for each conference, choice of themes, choice of location, representation of participating countries, refereeing standards, and scientific criteria
* Appointing the program-committee chair(s) and the other officers for each conference.
* Approving the major decisions of the program committee
* Approving the major decisions of the organizing committee

The steering committee is composed of the program chairs and general chairs of the past three and the three upcoming conferences (as soon as they are appointed). Furthermore, it contains the past steering committee chair, and representatives of the respective computer societies and individuals nominated by the steering committee because they are recognized as experts in the field.

The table below lists the current Steering Committee members. For questions, please do not hesitate to contact the steering committee chair. 

{% assign members = site.data.steering_committee | sort: "lastname" %}
{% for member in members %}
    {%- assign member_name = member.firstname | append: " " | append: member.lastname -%}
    {%- assign member_image = "assets/img/" | append: member.image -%}
|![{{ member_name }}]({{ member_image }})|[{{ member_name }}]({{ member.homepage }})<br>{{ member.affiliation }}<br>{{ member.position }}|
{% endfor %}{: id="sc-table" }


