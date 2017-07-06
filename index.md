---
layout: default
---

{% assign sorted_projects = site.projects | sort: "order" %}
<div class="portfolio-page">
{% for project in sorted_projects %}
	<a href="{{project.url}}">
		<div style="background-image:url('{% for feature in project.feature %}{{site.baseurl}}imgs/icons/{{feature.icon}}{% endfor %}');" id="{{project.slug}}" class="project-blob {{project.category}}">
			<div class="project-title">{{project.title}}</div>
		</div>
	</a>
{% endfor %}
</div>