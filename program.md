---
layout: program 
title: "Programs"
description: "Talks and posters" 
---


## Talks

**NB:** Click speaker and title to toggle abstract. ...


<!-- Tab links -->
<div class="tab">
  <!-- <button> </button> -->
  <button class="tablinks" onclick="openDate(event, 'cDay1')" id="defaultOpen">Mon 3 Aug</button>
  <button class="tablinks" onclick="openDate(event, 'cDay2')">Tue 4 Aug</button>
  <button class="tablinks" onclick="openDate(event, 'cDay3')">Wed 5 Aug</button>
  <button class="tablinks" onclick="openDate(event, 'cDay4')">Thu 6 Aug</button>
  <button class="tablinks" onclick="openDate(event, 'cDay5')">Fri 7 Aug</button>
</div>

<!-- Tab content -->
{% for item in site.data.dtalks.toc %}
<div id="{{ item.title }}" class="tabcontent">
    <table class="tg">
      <tr>
        <th class="tg-lboi" style="min-width:128px">Time</th>
        <th class="tg-lboi">Event</th>
      </tr>
	  {% if item.title == "cDay" %} <!-- "cDay1" -->
        <tr>
          <td class="tg-lboi"> 8:50 - 9:00 </td>
          <td class="tg-talk"> Opening remarks </td>
        </tr>
	  {% endif %}
	  {% for entry in item.talks %}
        <tr>
          <td class="tg-lboi"> {{ entry.ttime }} </td>
          <td class="tg-talk"> <details> <summary><a href="#talks">{{ entry.name }}</a>: {{ entry.ttitle }}</summary> <p class="abstract"><b>Abstract:</b> {{ entry.tabstract }} </p></details> </td>
        </tr>
	  {% endfor %}
    </table>
</div>
{% endfor %}



## Posters


<ul>
    {% for poster in site.data.posters %}
      <li>
        <details> <summary>{{ poster.name }}: {{ poster.title }}</summary> <i style="font-size:1.5rem;"><b style="padding-left:28px;">Abstract:</b> {{ poster.abstract }}</i></details>
      </li>
    {% endfor %}
</ul>


<!-- <table class="poster">
  <tr>
    <th class="poster-lboi" height="30" style="min-width:128px">Authors</th>
    <th class="poster-lboi" height="30">Title</th>
  </tr>
  {% for poster in site.data.posters %}
  <tr>
  	  <td class="poster-lboi" height="20"> {{ poster.name }}  </td>
  	  <td class="poster-title" height="20"> <details> <summary>{{ poster.title }}</summary><i><b>Abstract:</b> {{ poster.abstract }}</i></details> </td>
  </tr>
  {% endfor %}
</table> -->


