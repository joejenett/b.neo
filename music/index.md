---
layout: page
---
<script>document.title="𝗯𝘂𝗹𝗹𝘁𝗼𝘄𝗻.𝗻𝗲𝗼 | music"</script>

<h1>music:</h1>
<ul>
{% for post in site.posts %}
{% for category in site.categories %}

{% if post.categories contains "music" %}
{% assign count = 0 %}
{% assign count = count | plus:1 %}
<li><a href="{{ site.baseurl }}{{ post.permalink }}">{{ post.title }}</a>
        <date><small>({{ post.date | date:'%b %-d, %Y'}})</small></date></li>
{% if count == 1 %}{% break %}{% endif %}
{% endif %}

{% endfor %}
{% endfor %}
</ul>


