---
layout: home
title: Home
---

<div id="intro-wrapper" class="l-text">
	<div id="intro-title-wrapper">
		<div id="intro-image-wrapper">
			<img id="intro-image" src="/images/portrait.png"></div>
		<div id="intro-title-text-wrapper">
			<h1 id="intro-title">Hi, I'm Xuesong Nie</h1>
			<div id="intro-subtitle">I'm a M.S. Student at Zhejiang University</div>
			<div id="intro-title-socials">
				{% for link in site.data.social-links %}
					{% if link.on-homepage == true %}
						{% include social-link.html link=link %}
					{% endif %}
				{% endfor %}
			</div>
		</div>
	</div>
	<!-- <hr class="l-middle home-hr"> -->
	<div id="everything-else" class="l-middle">
		<a href="{{ site.url }}/cv"><div><i class="fa fa-portrait icon icon-right-space"></i>CV</div></a>
		<a href="{{ site.url }}/projects"><div><i class="fa fa-shapes icon icon-right-space"></i>Projects</div></a>
		<a href="{{ site.url }}/everything-else"><div><i class="fa fa-list-ul icon icon-right-space"></i>Everything Else</div></a>
	</div>
	<div>
		I am currently a second-year M.S. student in the Zhejiang University working on Computer Vision, supervised by Prof. <a href="https://person.zju.edu.cn/0004117">Donglian Qi</a>. Before that, I obtained a Bachelor of Science in Communication Engineering from Henan University. I have spent wonderful times as an intern with with Dr. <a href="https://xavierchen34.github.io/">Xi Chen</a> at Alibaba, and Prof. <a href="https://scholar.google.com/citations?hl=zh-CN&user=Y-nyLGIAAAAJ">Stan Z. Li</a> at <a href="https://www.westlake.edu.cn/">CAIRI AI Lab</a>.
	</div>
	<div style="height: 1rem"></div>
	<div>
		My long-term aspiration to help people <b>understand the world</b> with <b>machine learning models</b>. With this vision in mind, my current research interests and focus: 1. Spatiotemporal Predictive Learning; 2. Image / Video Perception; 3. Generative Models; 4. AI for Science. More experiences about me please refer to <a href="/cv">my CV</a>.
	</div>
	<div style="height: 1rem"></div>
	<div>
		I’m actively applying for CS/CV internships, RAs and Ph.D. positions in 2025 Spring or 2025 Fall. Feel free to email me for cooperations or potential interviews.
	</div>
</div>

<hr class="l-middle home-hr">

<h2 class="feature-title l-middle">Featured <a href="/cv/#publications">Research Publications</a></h2>

<p class="feature-text l-middle">
	My recent research for generative models, spatiotemporal predictive learning, and image / video perception.
</p>

<div class="cover-wrapper cover-wrapper-3-col l-middle">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.featured == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>

<br>
<h2 class="feature-title l-middle">Featured <a href="/dissertation">Dissertation Publications</a></h2>

<p class="feature-text l-middle">
	My recent research for open-source projects and everything else.
</p>

<div class="cover-wrapper cover-wrapper-1-col l-text">
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
