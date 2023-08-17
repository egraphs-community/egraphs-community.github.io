---
layout: default
title: EGRAPHS Community Meeting
---

We have a monthly community meeting on the third Thursday of each month at 9:00am Pacific time.

{% assign calendar = "http://egraphs.org/meeting/calendar.ics"%}

A calendar for these meetings can be found [here]({{calendar}}) in `.ics` format.
To add this to your Google Calendar, [click here](http://www.google.com/calendar/render?cid={{calendar}}), or add it manually by hitting "Other Calendars" → "+" → "From URL" and pasting the `.ics` link above.


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
