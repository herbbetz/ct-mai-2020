---
title: Jekyll
---
[Jekyll Doku](https://jekyllrb.com/docs/)

Jekyll ist ein Ruby Programm und baut die Website, auch auf Github.

+ Empfehlung: am MD-Dateianfang immer FrontMatter (2 Zeilen mit ---), sonst keine Verarbeitung von Liquid Template Variablen  
  am besten, nach Erstellung von `_layouts/default.html`:
  ```
  ---
  layout: default
  title: Wasauchimmer
  ---
  ```

+ Troubleshoot: 
  z.B. steht im FrontMatter statt `title: Markdown` nur `Markdown`, dann in Settings `website compile problems`   
  siehe [Troubleshoot Guide](https://help.github.com/en/github/working-with-github-pages/troubleshooting-jekyll-build-errors-for-github-pages-sites#troubleshooting-build-errors)
  
+ der Pfad / oder /index.html oder /about.html in _data/nav.yml bezieht sich auf https://herbbetz.github.io und nicht auf https://herbbetz.github.io/ct-mai-2020/. Auf letzteres bezieht sich aber {{page.url}}, das dadurch nicht einfach mit {{item.link}} aus site.data.nav vergleichbar ist. Vgl. Code aus https://jekyllrb.com/docs/step-by-step/06-data-files/

  Verwendung von _data/nav.yml in den Pages auf github.com also problematisch, da in site.data.nav der Repository-Name fuer funktionierenden Link extra eingefuegt werden muss, und dann mit page.url nicht mehr übereinstimmt...
  


