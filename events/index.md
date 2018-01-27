---
layout: default
title: Upcoming Events
description: Upcoming DATA TAS events
keywords: data,event,hobart,tasmania,workshop,seminar,conference
container: true
disable: true
show_banner: false
---

{% if page.disable %}

<div class="alert alert-info">We are in the process of scheduling our first series of events for 2018, please check back soon.</div>
<p>Looking for past events? <a href="/events/past">Click Here</a></p>

{% else %}
<table class="table table-bordered table-striped">

    <thead>
        <tr>
            <th width="20%">When/Where?</th>
            <th>Event</th>
        </tr>
    </thead>

    <tbody>

        {% for event in site.data.events %}
        {% if event.type == "upcoming" %}
        <tr>
            <td>{{event.date}} @ {{event.time}}<br/><em>{{event.venue}}</em></td>
            <td><strong>{{event.title}}</strong><br/>{{event.description}}
            {% if event.link %}<br/><a href="{{event.link}}" target="_blank">Details</a>{% endif %}</td>
        </tr>
        {% endif %}
        {% endfor %}

    </tbody>

</table>

<p>Looking for past events? <a href="/events/past">Click Here</a></p>

{% endif %}
