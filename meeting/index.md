---
layout: default
title: EGRAPHS Community Meeting
---

We have a monthly community meeting on the third Thursday of each month at 9:00am Pacific time.
Meetings are approximately 1 hour long.

The [Zoom link is here](https://berkeley.zoom.us/j/96954799525).

We are now recording the meetings and posting them on YouTube
 on the [EGRAPHS Community YouTube channel](https://www.youtube.com/@egraphs-community).

{% assign calendar = "http://egraphs.org/meeting/calendar.ics" %}

Add this to your Google Calendar by 
[clicking here](http://www.google.com/calendar/render?cid={{calendar}}), 
or add it manually by hitting 
"Other Calendars" → "+" → "From URL" and pasting this URL:
<code style="white-space: nowrap">{{calendar}}</code>

### Meetings

<style>
  .meeting.past { opacity: 50%; }
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
