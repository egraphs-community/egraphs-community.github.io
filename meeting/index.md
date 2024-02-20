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

<ul class="meetings">
{% for meeting in site.categories.meeting %}
  {% unless meeting.hide %}
  <li class="meeting" data-date="{{ meeting.date | date: "%Y-%m-%d" }}">
    <a href="{{meeting.url}}">
      <time>{{ meeting.date | date: "%Y-%m-%d" }}</time>:
      {{ meeting.title | default: "Meeting" }}
    </a>
  </li>
  {% endunless %}
{% endfor %}
</ul>

<!-- <script defer>
  // loop over all elements of class meeting
  var meetings = document.getElementsByClassName("meeting");
  console.log(meetings);
  for (let meeting of meetings) {
    // get the date of the meeting
    var date = meeting.getAttribute("data-date");
    // get the current date
    var now = new Date();
    // if the meeting is in the past, hide it
    if (now > new Date(date)) {
      meeting.style.opacity = "50%";
    }
    console.log(meetings);
  }

  console.log("hello")
</script> -->


