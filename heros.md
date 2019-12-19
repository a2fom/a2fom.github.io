---
layout: heros 
title: "Wall of the Heros"
description: "Agility, Intelligence and Strength" 
---



## Wall of heros


<!-- Tab links -->
<div class="tab" style="margin-top:1em;">
    <button class="tablinks" onclick="openDate(event, 'Agility')" id="defaultOpen" style="color:#16b67b;"> Agility </button>
    <button class="tablinks" onclick="openDate(event, 'Intelligence')" style="color:#1a8cff;"> Intelligence </button>
    <button class="tablinks" onclick="openDate(event, 'Strength')" style="color:#df1a8c;"> Strength </button>
    <button class="tablinks" onclick="openDate(event, 'Showall')" style="color:#6600ff;"> Show all </button>
</div>



<!-- Tab content -->
{% for item in site.data.heros.toc %}
<div id="{{ item.type }}" class="tabcontent">
    <p class="{{ item.style }}"><span> {{ item.type }} </span></p>
    <ul style="margin-left:0.725rem; padding:0;">
    {% for group in item.groups %}
            {% for hero in group.heros %}
            <!-- {{ hero.name }} -->
            <li style="display:inline-block;width: 150px;float: left;">
            <div class="icon_container">
              <a href="https://liquipedia.net/dota2/{{ hero.name }}"> <img src="assets/heros/{{ hero.filename }}" alt="{{ hero.name }}" style="width:150px;"></a>
              <div class="centered"> <a href="https://liquipedia.net/dota2/{{ hero.name }}"> <span class="hero_name"> {{ hero.name }}</span> </a> </div>
            </div>
            </li>
            {% endfor %}
    {% endfor %}
    </ul>
</div>
{% endfor %}



<!-- Show all heros -->
<div id="Showall" class="tabcontent">
    {% for item in site.data.heros.toc %}
        <p class="{{ item.style }}"><span> {{ item.type }} </span></p>
        <ul style="margin-left:0.725rem; padding:0;">
        {% for group in item.groups %}
            {% for hero in group.heros %}
            <!-- {{ hero.name }} -->
            <li style="display:inline-block;width: 150px;float: left;">
                <div class="icon_container">
                  <a href="https://liquipedia.net/dota2/{{ hero.name }}"> <img src="assets/heros/{{ hero.filename }}" alt="{{ hero.name }}" style="width:150px;"></a>
                  <div class="centered"> <a href="https://liquipedia.net/dota2/{{ hero.name }}"> <span class="hero_name"> {{ hero.name }}</span> </a> </div>
                </div>
            </li>
           {% endfor %}
        {% endfor %}
        </ul>
    {% endfor %}
</div>






{{ site.data.heros.toc[0].groups[0].heros[0].lore[1] }}



## Lores of heros


**NB:** Click speaker and title to toggle lores...



<!-- Show all talks -->
<!-- <div id="Showallhero" class="tabcontent"> -->
<table class="tg" style="width:96%;table-layout:fixed;border:1px solid rgb(222,222,222); margin-left:auto;margin-right:auto;">
    {% for item in site.data.heros.toc %}
      <tr>
        <th class="lore" style="border:1px solid rgb(222,222,222);">{{ item.type }} heros</th>
        <th class="lore" style="width:100%;border:1px solid rgb(222,222,222);">Lores</th>
      </tr>
      {% for group in item.groups %}
        {% for hero in group.heros %}
        <tr>
          <td class="tg-time" style="border:1px solid rgb(222,222,222);"> {{ hero.name }} </td>
          <td class="tg-talk" style="border:1px solid rgb(222,222,222);"> <details> <summary><a>{{ entry.name }}</a> {{ hero.name }}</summary> <p class="abstract"><b>Lore:</b> {{ hero.lore }} </p></details> </td>
        </tr>
        {% endfor %}
      {% endfor %}
    {% endfor %}
</table>
<!-- </div> -->





<!-- <ul>
    {% for poster in site.data.posters %}
      <li>
        <details> <summary>{{ poster.name }}: {{ poster.title }}</summary> <i style="font-size:1.5rem;"><b style="padding-left:28px;">Abstract:</b> {{ poster.abstract }}</i></details>
      </li>
    {% endfor %}
</ul> -->













  

