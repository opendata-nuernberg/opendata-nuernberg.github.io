---
layout: page
title: Code for Nürnberg & Fürth
subtitle: Freie Software & Offene Daten für eine lebenswertere Stadt
hero_height: is-medium
hero_is_landingpage: true
show_sidebar: false
---


## Wer sind wir?

"Code for Nürnberg-Fürth" ist ein lockerer Zusammenschluss von Menschen, die in ihrer Freizeit ehrenamtlich auf mehr Transparenz der Politik und Verwaltung hinwirken wollen. Dazu versuchen wir Datenschätze der öffentlichen Hand (Stadt, Stadtwerke, etc.) für die Allgemeinheit zu öffnen und zugänglich zu machen. Aus diesen offenen Daten erstellen wir offene und freie Anwendungen, von der die Stadtgesellschaft profitieren soll.

## Weitere Termine

{% include events_showcase.html %}


## Projekte

{% include projects_showcase.html %}

### Weitere Projekte

{% include projects.html %}

## Aktuelle Blog-Artikel

{% for post in site.posts limit:2 %}
{% include blogpost_link.html post=post %}
{% endfor %}
