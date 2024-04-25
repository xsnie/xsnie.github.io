---
layout: page
title: Projects
permalink: projects/
---

Things I do, including research, academic course projects, and miscellaneous interests.

## Related Research

My recent research for open-source projects and everything else.

<div class="cover-wrapper cover-wrapper-1-col l-middle">
	{% include dissertation/document.html details=false location=home %}
</div>

<div class="cover-wrapper cover-wrapper-3-col l-middle">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.dissertation == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>

<div class="project-spacer-small"></div>

## Research

My recent research for generative models, predictive learning, and visual perception.

<div class="project-spacer-small"></div>

<div class="l-middle project-grid">
    {% for project in site.categories.papers %}
    {% include project.html project=project %}
    {% endfor %}
</div>

<div class="project-spacer"></div>

