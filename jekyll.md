---
layout: default
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
+ Auch SCSS-Dateien brauchen ein leeres solches FrontMatter am Anfang.

+ Troubleshoot: 
  z.B. steht im FrontMatter statt `title: Markdown` nur `Markdown`, dann in Settings `website compile problems`   
  siehe [Troubleshoot Guide](https://help.github.com/en/github/working-with-github-pages/troubleshooting-jekyll-build-errors-for-github-pages-sites#troubleshooting-build-errors)
  
+ der Pfad / oder /about.html in _data/nav.yml bezieht sich leider auf https://herbbetz.github.io und nicht auf https://herbbetz.github.io/ct-mai-2020/. Der Repository-Name muss per Liquid in _include/nav.html oder /blogs.html extra angehängt werden:

{% comment %}

```
 {% for item in site.data.nav %} 
    <a href="{{ "/ct-mai-2020" |append: item.link }}" {% if page.url == item.link %}class="current"{% endif %}>
      {{ item.name }}
    </a>
  {% endfor %}
```

---------------

```
  {% for post in site.posts %}
    <li>
      <h2><a href="{{"/ct-mai-2020" |append: post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
```

{% endcomment %}

+ Leider kann man in einem Markdown-Codeblock (3 Hochkommas) kein Liquid-Template-Code darstellen, ohne dass er ausgeführt wird. Auch `<pre><code>` hilft nicht, am ehesten hilft Liquids `{% comment %}{% endcomment %}`. 
