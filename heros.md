---
layout: heros 
title: "Wall of the Heros"
description: "Agility, Intelligence and Strength" 
---



## Wall of heros


<!-- Tab links -->
<div class="tab">
    <button class="tablinks" onclick="openDate(event, 'Agility')" id="defaultOpen" style="color:#1acf8c;"> Agility </button>
    <button class="tablinks" onclick="openDate(event, 'Intelligence')" style="color:#1a8cff;"> Intelligence </button>
    <button class="tablinks" onclick="openDate(event, 'Strength')" style="color:#df1a8c;"> Strength </button>
    <button class="tablinks" onclick="openDate(event, 'Showall')" style="color:#6600ff;"> Show all </button>
</div>



<!-- Tab content -->
{% for item in site.data.heros.toc %}
<div id="{{ item.type }}" class="tabcontent">
    <table class="tg">
      <tr>
      <th colspan="6" style="text-align:center;">{{ item.type }}</th>
      </tr>
      {% for group in item.groups %}
          <tr>
              {% for hero in group.heros %}
              <!-- {{ hero.name }} -->
              <td>
              <div class="icon_container">
                <img src="assets/heros/{{ hero.filename }}" alt="{{ hero.name }}" style="width:100%;">
                <div class="centered"> <span class="hero_name"> {{ hero.name }}</span> </div>
              </div>
              </td>
              {% endfor %}
          </tr>
      {% endfor %}
    </table>
</div>
{% endfor %}



<!-- Show all heros -->
<div id="Showall" class="tabcontent">
    {% for item in site.data.heros.toc %}
    <table class="hero_tg">
      <tr>
      <th colspan="6" style="text-align:center;">{{ item.type }}</th>
      </tr>
      {% for group in item.groups %}
          <tr>
              {% for hero in group.heros %}
              <!-- {{ hero.name }} -->
              <td>
              <div class="icon_container">
                <img src="assets/heros/{{ hero.filename }}" alt="{{ hero.name }}" style="width:100%;">
                <div class="centered"> <span class="hero_name"> {{ hero.name }}</span> </div>
              </div>
              </td>
              {% endfor %}
          </tr>
      {% endfor %}
    </table>
    {% endfor %}
</div>






## Workshops

**NB:** Click speaker and title to toggle abstract. ...


<!-- Tab links -->
<div class="tab">
    {% for item in site.data.dtalks.toc %}
      {% if item.title == "cDay1" %} <!-- "cDay1" -->
          <button class="tablinks" onclick="openDate(event, '{{ item.title }}')" id="defaultOpen"> {{ item.date }} </button>
      {% else %}
          <button class="tablinks" onclick="openDate(event, '{{ item.title }}')"> {{ item.date }} </button>
      {% endif %}
    {% endfor %}
    <button class="tablinks" onclick="openDate(event, 'Showallhero')" style="color:#1a8cff;"> Show all </button>
</div>


<!-- Tab content -->
{% for item in site.data.dtalks.toc %}
<div id="{{ item.title }}" class="tabcontent">
    <table class="tg">
      <tr>
        <th class="tg-time">Time</th>
        <th class="tg-talk">Event</th>
      </tr>
      {% if item.title == "cDay1" %} <!-- "cDay1" -->
        <tr>
          <td class="tg-time"> 9:00 - 9:50 </td>
          <td class="tg-talk"> <details> <summary><a href="#talks">Axe</a>: All Heros Are Created Equal, Yet We Are The Only One Suffering!</summary> <p class="abstract"><b>Abstract:</b> {{ entry.tabstract }} </p></details> </td>
        </tr>
      {% endif %}
	  {% for entry in item.talks %}
        <tr>
          <td class="tg-time"> {{ entry.ttime }} </td>
          <td class="tg-talk"> <details> <summary><a href="#talks">{{ entry.name }}</a>: {{ entry.ttitle }}</summary> <p class="abstract"><b>Abstract:</b> {{ entry.tabstract }} </p></details> </td>
        </tr>
	  {% endfor %}
    </table>
</div>
{% endfor %}


<!-- Show all talks -->
<div id="Showallhero" class="tabcontent">
    {% for item in site.data.dtalks.toc %}
    <table class="tg">
      <tr>
        <th class="tg-time">{{ item.date }}</th>
        <th class="tg-talk">Event</th>
      </tr>
	  {% if item.title == "cDay1" %} <!-- "cDay1" -->
        <tr>
          <td class="tg-time"> 8:50 - 9:00 </td>
          <td class="tg-talk"> Opening remarks </td>
        </tr>
	  {% endif %}
	  {% for entry in item.talks %}
        <tr>
          <td class="tg-time"> {{ entry.ttime }} </td>
          <td class="tg-talk"> <details> <summary><a href="#talks">{{ entry.name }}</a>: {{ entry.ttitle }}</summary> <p class="abstract"><b>Abstract:</b> {{ entry.tabstract }} </p></details> </td>
        </tr>
	  {% endfor %}
    </table>
    {% endfor %}
</div>






 <!-- Tab links -->
<div class="tab">
  <button class="tablinks" onclick="openDate(event, 'London')">London</button>
  <button class="tablinks" onclick="openDate(event, 'Paris')">Paris</button>
  <button class="tablinks" onclick="openDate(event, 'Tokyo')">Tokyo</button>
</div>

<!-- Tab content -->
<div id="London" class="tabcontent">
  <h3>London</h3>
  <p>London is the capital city of England.</p>
</div>

<div id="Paris" class="tabcontent">
  <h3>Paris</h3>
  <p>Paris is the capital of France.</p>
</div>

<div id="Tokyo" class="tabcontent">
  <h3>Tokyo</h3>
  <p>Tokyo is the capital of Japan.</p>
</div> 




<!-- ## Details


<ul>
    {% for poster in site.data.posters %}
      <li>
        <details> <summary>{{ poster.name }}: {{ poster.title }}</summary> <i style="font-size:1.5rem;"><b style="padding-left:28px;">Abstract:</b> {{ poster.abstract }}</i></details>
      </li>
    {% endfor %}
</ul> -->


<!-- <table class="poster">
  <tr>
    <th class="poster-lboi" height="30">Authors</th>
    <th class="poster-lboi" height="30">Title</th>
  </tr>
  {% for poster in site.data.posters %}
  <tr>
  	  <td class="poster-lboi" height="20"> {{ poster.name }}  </td>
  	  <td class="poster-title" height="20"> <details> <summary>{{ poster.title }}</summary><i><b>Abstract:</b> {{ poster.abstract }}</i></details> </td>
  </tr>
  {% endfor %}
</table> -->





  

