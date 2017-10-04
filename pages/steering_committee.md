---
title: Steering Committee
order: 4
---
The ESEC/FSE Steering Committee is responsible for constituting and guiding each edition of ESEC/FSE and for establishing and evaluating practices that are binding upon the organizers of each conference for the continued technical and financial success of ESEC/FSE.

In particular, the ESEC/FSE Steering Committee is the body responsible for the long term policy of the conference series. 

Its tasks are the following ones:

* Defining the scope, aims, and long-term evolution of the series.
* Establishing the rules governing choice of officers for each conference, choice of themes, choice of location, 
representation of participating countries, refereeing standards, scientific criteria.
* Appointing the program chair(s) and the other officers for each conference.
* Approving the major decisions of the program committee.
* Approving the major decisions of the organizing committee.

The table below lists the current ESEC/FSE Steering Committee members. For questions you can contact the SC Chair. 

{% assign members = site.data.steering_committee | sort: "lastname" %}
{% for member in members %}
    {%- assign member_name = member.firstname | append: " " | append: member.lastname -%}
    {%- assign member_image = "assets/img/" | append: member.image -%}
|![{{ member_name }}]({{ member_image }})|[{{ member_name }}]({{ member.homepage }})<br>{{ member.affiliation }}<br>{{ member.position }}|
{% endfor %}{: id="sc-table" }

The steering committee is composed of the program chairs and general chairs of past conferences, the program chair and general chair of 
the next conference (as soon as they are appointed), representatives of the respective computer societies, and 
individuals nominated by the steering committee because they are recognized as experts in the field.

The term for steering-committee members is six years. The total number of members of the steering committee cannot exceed 15 and must be, at least, 8.
