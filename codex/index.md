---
layout: default
show_banner: true
title: CODEX
description: Master list of helpful data and science links
container: true
---

<div class="alert alert-info">
Want to add something to the CODEX? <a href="https://github.com/datatas/datatas.github.io/issues/new?title=Codex Contribution&body=Thank%20you%20for%20offering%20to%20contribute%20to%20the%20CODEX,%20please%20provide%20the%20title,%20url%20and%20description%20of%20the%20site%20you'd%20like%20to%20see%20added.&labels[]=codex" target="_blank">Click Here</a>
</div>

<table class="table table-striped table-full">

{% for topic in site.data.codex %}

<tr>
    <td colspan="2"><strong>{{ topic.heading }}</strong></td>
</tr>

{% for link in topic.links %}
<tr>
    <td width="30%">
        {{ link.title }}<br/>
        <a href="{{ link.url }}" target="_blank">{{ link.url }}</a>
    </td>
    <td>
        {{ link.description }}
    </td>
</tr>
{% endfor %}

{% endfor %}

</table>