---
layout: default
title: EGRAPHS Community Meeting
---

We have a monthly community meeting on the third Thursday of each month at 9:00am Pacific time.

{% assign calendar = "http://egraphs.org/meeting/calendar.ics" %}

A calendar for these meetings can be found [here]({{calendar}}) in `.ics` format.
To add this to your Google Calendar, [click here](http://www.google.com/calendar/render?cid={{calendar}}), or add it manually by hitting "Other Calendars" → "+" → "From URL" and pasting the `.ics` link above.


### Meetings

<ul class="meetings">
{% for meeting in site.categories.meeting %}
  <li class="meeting" data-date="{{ meeting.date | date: "%Y-%m-%d" }}">
    <a href="{{meeting.url}}">
      <time>{{ meeting.date | date: "%Y-%m-%d" }}</time>:
      {{ meeting.title | default: "Meeting" }}
    </a>
    {{ meeting.excerpt }}
  </li>
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


