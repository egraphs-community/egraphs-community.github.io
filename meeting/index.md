---
layout: default
title: EGRAPHS Community Meeting
---

We have a monthly community meeting on the third Thursday of each month at 9:00am Pacific time.

A calendar for these meetings can be found [here](calendar.ics) in `.ics` format.
To add this to your Google Calendar, [click here](http://www.google.com/calendar/render?cid={{site.url}}{{page.url}}calendar.ics).


### Meetings

<ul class="meetings">
{% for meeting in site.categories.meeting %}
  {% unless meeting.hide %}
  <li>
    {{ meeting.date | date: "%Y-%m-%d" }}:
    <a href="{{meeting.url}}">
      {{ meeting.title | default: "Meeting" }}
    </a>
  </li>
  {% endunless %}
{% endfor %}
</ul>
