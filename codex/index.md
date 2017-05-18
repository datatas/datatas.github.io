---
layout: default
show_banner: true
title: CODEX
description: Code examples repository
container: false
disabled: true
---

<div class="container">

    <div class="row">

        <div class="col-sm-7">

            <p class="lead">
                Welcome to the Code Examples Repository (CODEX),<br/>
                <br/>
                The CODEX is designed to ease the pressure on newcomers to data analysis and programming through a series of step-by-step tutorials following a logical curriculum that spans multiple programming languages.<br/>
                <br/>
                This repository is open access and maintained by the DataTas community, starting from the fundamentals and moving onto more advanced techniques.<br/>
                <br/>
                The CODEX curriculum is currently under development, please check back soon.

            </p>

        </div>

        <div class="col-sm-5">

            <img src="/img/logo-codex.svg" alt="CODEX logo"/>

        </div>

    </div>

    {% if page.disabled == false %}

    <div class="row">

        {% for stream in site.data.codex %}

        <div class="{{stream[1].parent_class}}">
            <a href="/codex/{{stream[1].slug}}" class="stream-tile stream-shell stream-{{stream[1].slug}}">
                <span class="stream-title">{{stream[1].title}}</span>
                <span class="stream-description">{{stream[1].description}}</span>
                <span class="stream-meta">{{stream[1].topics | size}} topics</span>
            </a>
        </div>

        {% endfor %}

    </div>

    {% endif %}

</div>
