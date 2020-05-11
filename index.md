---
layout: default
title: Web-IF
---
## Website-Gestaltung im Webinterface

+ Nur der master branch steht für Website zur Auswahl in settings. 

+ Die index.html ist sowieso nirgends sichtbar und wird wohl dynamisch erzeugt? Es sollten aber doch statische Websites sein? Download mit WGET?

+ Caching: Website erst nach wiederholtem Laden aktuell.

+ Das Hochladen von Dateien in Ordnern ist in der Github-Weboberfläche sehr umständlich: New File - Ordnername/d.txt, dann Datei dorthin hochladen, denn d.txt mit TrashIcon und Commit deleten... Nur mit GIT-Commandline praktikabel...

+ der Pfad / oder /index.html oder /about.html in _data/nav.yml bezieht sich auf https://herbbetz.github.io und nicht auf https://herbbetz.github.io/ct-mai-2020/. Auf letzteres bezieht sich aber {{page.url}}, das dadurch nicht einfach mit {{item.link}} aus site.data.nav vergleichbar ist. Vgl. Code aus https://jekyllrb.com/docs/step-by-step/06-data-files/

  Verwendung von _data/nav.yml also problematisch, da in site.data.nav der Repository-Name fuer funktionierenden Link 
extra eingefuegt werden muss, und dann mit page.url nicht mehr übereinstimmt...
