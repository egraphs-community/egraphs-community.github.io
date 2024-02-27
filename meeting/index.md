---
layout: default
title: EGRAPHS Community Meeting
---

We have a monthly community meeting on the third Thursday of each month at 9:00am Pacific time.
Meetings are approximately 1 hour long.

The Zoom link will be distributed on the [EGRAPHS Zulip](/zulip)
 just in time for each session.

{% assign calendar = "http://egraphs.org/meeting/calendar.ics" %}

Add this to your Google Calendar by 
[clicking here](http://www.google.com/calendar/render?cid={{calendar}}), 
or add it manually by hitting 
"Other Calendars" → "+" → "From URL" and pasting this URL:
<code style="white-space: nowrap">{{calendar}}</code>

### Meetings

<style>
  .meeting.past { opacity: 50%; }
  .meeting.future:has(+ .past) { 
    font-weight: bold;
  }
</style>

<ul class="meetings">
{% for meeting in site.categories.meeting %}
  <li class="meeting" data-date="{{ meeting.date | date: "%Y-%m-%d" }}">
    {% capture text %}
        <time>
        {{ meeting.date | date: "%Y-%m-%d" }}</time>:
        {{ meeting.title | default: "Meeting" }}
        {% if meeting.speaker %}
          ({{ meeting.speaker }})
        {% endif %}
    {% endcapture %}
    {% if meeting.hide %}
      {{ text }}
    {% else %}
      <a href="{{meeting.url}}"> {{ text }} </a>
    {% endif %}
  </li>
{% endfor %}
</ul>

<script defer>
  const meetingElements = document.querySelectorAll('.meeting');
  const currentDate = new Date();

  meetingElements.forEach((meetingElement) => {
    const meetingDate = new Date(meetingElement.dataset.date);

    if (meetingDate > currentDate) {
      meetingElement.classList.add('future');
    } else {
      meetingElement.classList.add('past');
    }
  });
</script>


