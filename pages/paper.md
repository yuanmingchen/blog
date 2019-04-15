---
layout: page
title: 论文
tagline: 论文笔记
keywords: 论文, paper
comments: true
permalink: /paper/
---

<ul class="listing">
{% for paper in site.categories.paper %}
{% if paper.title != "paper Template" %}
	<li class="listing-item"><a href="{{ site.url }}{{ paper.url }}">{{ paper.title }}</a>
        <div class="collection-info">
          {% if paper.date %}
			<span class="meta-info">
				<span class="octicon octicon-calendar"></span> {{ paper.date | date: "%Y/%m/%d" }}
			</span>
          {% endif %}
        </div>
	</li>
	<br/>
{% endif %}
{% endfor %}
</ul>
