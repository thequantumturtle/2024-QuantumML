---
# title: Schedule
# layout: page
# menuItem: Schedule
# menuPosition: 2
---
{% if site.docsUrl != "" %}
You can download all required reading in the [Study materials]({{ site.docsUrl }}) at the faculty website.
{% endif %}

<ol>
{% assign syllabus = site.syllabus | sort: "lecture" %}
{% for lecture in syllabus %}
  <li>
  	<a href="{{ site.baseurl }}{{ lecture.url }}">{{ lecture.title }}</a> 
  	{% for tag in lecture.tags %}
  		<b>#{{ tag }}</b>
  	{% endfor %}
  	({{ lecture.day }})</li>
{% endfor %}
</ol>
