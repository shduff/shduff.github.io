---
layout: default
---

<style>
a {
	text-decoration: none;
}
div#logotype {
	position:fixed;
	right:1em;
	bottom:0;
	font-family:Courier;
	font-size:2.5em;
	text-align:right;	
}
div#logotype h1 {
	margin:.2em;
}
div.social-media {
	height:1em;
	width:1em;
	display:inline-block;
	border:solid 1px #aaa;
	border-radius:.1em;
	text-align:right;
}
div#nav {
	position:fixed;
	right:1em;
	top:1em;
	text-align:right;
}
div#nav ul {
	font-family:Courier;
	list-style-type:none;
}
div#nav ul a {
	text-decoration:none;
	color:black;
}
div#nav ul a:hover {
	color:#aaa;
}
div.project-zone {
	width:60%;
	height:100%;
	text-align:left;
}
div.project-zone .project-blob {
	height:13em;
	width:13em;
	border-radius:2em;
	background-size:cover;
	display:inline-block;
}
div.project-zone .project-title {
	text-align:center;
	font-family:Courier;
	color:black;
	/*background-color:rgba(255,255,255,.5);*/
	margin-top:11em;
	font-size:1.2em;
	font-weight:bold;
}

/*div.project-zone .edu {
	box-shadow:0px 0px 10px blue inset;
	border:solid 1px blue;
}
div.project-zone .poetry {
	box-shadow:0px 0px 10px pink inset;
	border:solid 1px pink;
}
div.project-zone .music {
	box-shadow:0px 0px 10px orange inset;
	border:solid 1px orange;
}*/
</style>

{% assign sorted_projects = site.projects | sort: "order" %}
<div class="project-zone">
{% for project in sorted_projects %}
	<a href="{{project.url}}">
		<div style="background-image:url('{% for feature in project.feature %}{{site.baseurl}}imgs/{{feature.icon}}{% endfor %}');" id="{{project.slug}}" class="project-blob {{project.category}}">
			<div class="project-title">{{project.title}}</div>
		</div>
	</a>
{% endfor %}
</div>

<div id="nav">
	<ul>
		<a href=""><li class="edu">EDU</li></a>
		<a href=""><li class="music">MUSIC</li></a>
		<a href=""><li class="poetry">POETRY</li></a>
		<a href=""><li>NOTEBOOK</li></a>
		<a href=""><li>CONTACT</li></a>
	</ul>
</div>

<div id="logotype">
	<a href="mailto:{{site.email}}"><div id="email" class="social-media"> </div></a>
	<a href="http://twitter.com/{{site.twitter_username}}"><div id="twitter" class="social-media"> </div></a>
	<a href="http://facebook.com/{{site.facebook_username}}"><div id="facebook" class="social-media"> </div></a>
	<a href="http://github.com/{{site.github_username}}"><div id="github" class="social-media"> </div></a>
	<h1>shaunalynn<br>duffy</h1>

</div>