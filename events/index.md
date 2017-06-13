---
layout: default
title: Upcoming Events
description: Upcoming DATA TAS events
keywords: data,event,hobart,tasmania,workshop,seminar,conference
container: true
disable: false
show_banner: false
---

{% if page.disable %}

<div class="alert alert-info">We are in the process of scheduling our first series of events, please check back soon.</div>

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
        <tr>
            <td>{{event.date}} @ {{event.time}}<br/><em>{{event.venue}}</em></td>
            <td><strong>{{event.title}}</strong><br/>{{event.description}}
            {% if event.link %}<br/><a href="{{event.link}}" target="_blank">Details</a>{% endif %}</td>
        </tr>
        {% endfor %}

    </tbody>

</table>

{% endif %}
