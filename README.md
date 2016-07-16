*/ Conferences
-----------------------------------





*/ Sessions
-----------------------------------






*/ Pages (Structure)
-----------------------------------






*/ SPEAKERS
-----------------------------------
-Name              / {{ entry.speaker-name }}
-Title             / {{ entry.speaker-organisation }}
-Photo             / {{ entry.speaker-photo }}
-Twitter           / {{ entry.speaker-twitter }}
-Content Related   / {{ entry.speaker-relatedcontent }}
- 

MwabukaMabassa021@



*/ EVENTS
-----------------------------------

-Dates              {{ entry.event-date }}
-Location           {{ entry.event-location }}
-Event Name         {{ entry.event-name }}
-Speakers           {{ entry.event-speakers }}
-Program            {{ entry.event-program }}
-Venue              {{ entry.event-venue }}
-Register link {{ entry.event-registrationlink }}
-Sponsors & partners {{ entry.event-sponsors }}


*/ SPONSORS
-----------------------------------

- Logo {{ entry.sponsor-logo }}
- Link {{ entry.sponsor-link }} 




*/ CODES
-----------------------------------





{% if image %}
 <a class="pull-right" href="{{ url }}"> 
   <figure class="placeholder">
     <img src="{{ image.getUrl('small') }}" alt="{{ image.title }}" >
   </figure> 
 </a>
{% endif %}
