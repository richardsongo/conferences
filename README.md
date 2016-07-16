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
<li>Content Related   / {{ entry.speaker-relatedcontent }}</li>
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
<li>- Logo {{ entry.sponsor-logo }}</li>
<li>- Link {{ entry.sponsor-link }} </li>
</ul>



CODES
-----------------------------------



<blockquote>

{% if image %}
 <a class="pull-right" href="{{ url }}"> 
   <figure class="placeholder">
     <img src="{{ image.getUrl('small') }}" alt="{{ image.title }}" >
   </figure> 
 </a>
{% endif %}

</blockquote>
