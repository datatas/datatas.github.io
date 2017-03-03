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

<div class="alert alert-info">We are in the process of scheduling our first series of events, please check back soon.</div>

{% else %}
<table class="table table-bordered table-striped">

    <thead>
        <tr>
            <th width="20%">Date</th>
            <th>Event</th>
        </tr>
    </thead>

    <tbody>

        {% for event in site.data.events %}
        <tr>
            <td>{{event.date}} @ {{event.time}}</td>
            <td>{{event.title}}<br/>{{event.description}}</td>
        </tr>
        {% endfor %}

    </tbody>

</table>

## Seminar Series

We meet monthly for our regular Seminar Series during which a handful of presenters will conduct a seminar on a data-related subject relevant to their work.

## Casual Meetups

Members meet casually to discuss code and data-related topics over a cuppa. If you require assistance or just want to bounce ideas off fellow data enthusiasts, this is the place for you.

- IMAS Waterfront, 9:00am Flex Space
- UTas Sandy Bay,

### R Fridays

Talk about R stuff...

{% endif %}
