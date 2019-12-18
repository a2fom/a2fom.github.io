---
layout: workshop 
title: "Workshop of the Heros"
description: "Talks and posters" 
---


## Talks

**NB:** Click speaker and title to toggle abstract. ...


<!-- Tab links -->
<div class="tab">
    {% for item in site.data.dtalks.toc %}
      {% if item.title == "cDay1" %} <!-- "cDay1" -->
          <button class="tablinks" onclick="openDate(event, '{{ item.title }}')" > {{ item.date }} </button>
      {% else %}
          <button class="tablinks" onclick="openDate(event, '{{ item.title }}')"> {{ item.date }} </button>
      {% endif %}
    {% endfor %}
    <button class="tablinks" onclick="openDate(event, 'Showall')" style="color:#1a8cff;" id="defaultOpen"> Show all </button>
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
</div>
{% endfor %}

<!-- Show all talks -->
<div id="Showall" class="tabcontent">
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



  

