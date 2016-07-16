
At a high level, we are settling on four content types:
<ul>
<li>Speakers</li>
<li>Events</li>
<li>Sessions</li>
<li>Pages</li>
</ul>
Those content types would be related together in the following ways:
<ul>
<li>Speakers relate to Sessions</li>
<li>Sessions relate to Events (via a Program matrix)</li>
<li>Pages relate to Events</li>
<li>Sponsors relate to Events</li>
</ul>
Conferences
-----------------------------------





Sessions
-----------------------------------






Pages (Structure)
-----------------------------------






SPEAKERS
-----------------------------------
<ul>
<li>Name              / {{ entry.speaker-name }}</li>
<li>Title             / {{ entry.speaker-organisation }}</li>
<li>Photo             / {{ entry.speaker-photo }}</li>
<li>Twitter           / {{ entry.speaker-twitter }}</li>
<li>Biography           / {{ entry.speaker-bio }}</li>
<li>Related Presentations   / {{ entry.speaker-relatedpresentations }}</li>
</ul>


EVENTS
-----------------------------------
<ul>
<li>Dates              {{ entry.event-date }}</li>
<li>Location           {{ entry.event-location }}</li>
<li>Event Name         {{ entry.event-name }}</li>
<li>Speakers           {{ entry.event-speakers }}</li>
<li>Program            {{ entry.event-program }}</li>
<li>Venue              {{ entry.event-venue }}</li>
<li>Register link {{ entry.event-registrationlink }}</li>
<li>Sponsors & partners {{ entry.event-sponsors }}</li>
</ul>

SPONSORS
-----------------------------------
<ul>
<li>Logo {{ entry.sponsor-logo }}</li>
<li>Link {{ entry.sponsor-link }} </li>
</ul>



CODES
-----------------------------------

<pre>
<code>

{% for speaker in entry.eventSpeakers %}
  
  <h2><a class="speaker-title" href="{{ speaker.url }}">{{ speaker.title }}</a></h2>
  <div>{{ speaker.organization }}</div>
  <a class="speaker-twittwe" href="{{ speaker.speaker-twitter }}">{{ speaker.speaker-twitter }}</a>
  
  {% if speaker.speaker-photo %}
  <a class="speaker-photo" href="{{ speaker.url }}">
  <img src="{{ image.getUrl('small') }}" alt="{{ image.title }}" >
  </a>
  {% endif %}
  
  <div>{{ speaker.speaker-bio }}</div>
  
  
  {% set relatedPresentations = craft.entries.section('workshops').relatedTo(speaker) %}
  {% for relatedPresentation in relatedPresentations %}
  <h3><a class="program-title" href="{{ relatedPresentation.url }}">{{ relatedPresentation.title }}</a></h3>
  {% endfor %}


{% endfor %}

</code>
</pre>



<pre>
<code>

{% if image %}
 <a class="pull-right" href="{{ url }}"> 
   <figure class="placeholder">
     <img src="{{ image.getUrl('small') }}" alt="{{ image.title }}" >
   </figure> 
 </a>
{% endif %}

</code>
</pre>

