---
layout: default
title: EGRAPHS Community Meeting
---

We have regular, open community meetings to present work. Any and all are welcome to join!
If you have recommendations (including self-nominations) for speakers, please
 contact the [organizers](/about/).

{% assign calendar = "http://egraphs.org/meeting/calendar.ics" %}

- 📅 Meetings are the 3rd Thursday of each month at 9:00am Pacific time
  - [Add to Google Calendar](http://www.google.com/calendar/render?cid={{calendar}})
  - or add it manually by hitting "Other Calendars" → "+" → "From URL" and pasting:
    <code style="white-space: nowrap">{{calendar}}</code>
- 📹 [Zoom link](https://berkeley.zoom.us/j/96954799525)
- 📺 [YouTube Channel](https://www.youtube.com/@egraphs-community) for recordings

### Meetings

<style>
  .meeting { margin-bottom: 0.3em; }
  .meeting.past { opacity: 50%; }
  .meeting.future:has(+ .past) {
    margin-bottom: 2em;
  }
  .meeting.future:has(+ .past)::marker {
    color: red;
  }
</style>

<ul class="meetings">
{% for meeting in site.categories.meeting %}
  {% unless meeting.draft %}
  <li class="meeting" data-date="{{ meeting.date | date: "%Y-%m-%d" }}">
    <time>{{ meeting.date | date: "%Y-%m-%d" }}</time>:
    {% capture text %}
        {{ meeting.title | default: "Meeting" }}
    {% endcapture %}
    {% if meeting.hide %}
      {{ text }}
    {% elsif meeting.speaker %}
      {{ meeting.speaker }}
      <!-- {% if meeting.video %}📹{% endif %} -->
      <br>
      <a href="{{meeting.url}}"> {{ text }} </a>
    {% else %}
      <a href="{{meeting.url}}"> {{ text }} </a>
    {% endif %}
  </li>
  {% endunless %}
{% endfor %}
</ul>
