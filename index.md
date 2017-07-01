---
layout: default
---

<style>
a {
	text-decoration: none;
}
div#right-bar {
	position:fixed;
	/*background-color:#F1F1F1;*/
	height:100%;
	width:36%;
	top:0;
	right:0;
	/*border-right:1px #aaa;*/
	/*box-shadow:0px 0px 5px black inset;*/
}
div#logotype {
	position:absolute;
	bottom:1em;
	right:1em;
	font-family:Courier;
	font-size:2em;
	text-align:right;
}
div#logotype h1 {
	margin: 0em;
}
div.social-media {
	background-size:cover;
	height:2.2em;
	width:2.2em;
	margin:auto;
	display:inline-block;
	border:solid 1px #aaa;
	border-radius:.3em;
	text-align:right;
	box-shadow:0px 0px 5px black inset;

}
#email {
	background-image:url(../imgs/sm-email.PNG);
}
#twitter {
	background-image:url(../imgs/sm-twitter.PNG);
}
#facebook {
	background-image:url(../imgs/sm-facebook.PNG);
}
#github {
	background-image:url(../imgs/sm-github.PNG);
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

<!-- <div id="nav">
	<ul>
		<a href=""><li class="edu">EDU</li></a>
		<a href=""><li class="music">MUSIC</li></a>
		<a href=""><li class="poetry">POETRY</li></a>
		<a href=""><li>NOTEBOOK</li></a>
		<a href=""><li>CONTACT</li></a>
	</ul>
</div> -->

<div id="right-bar">
	<div id="logotype">
		<a href="mailto:{{site.email}}"><div id="email" class="social-media"> </div></a>
		<a href="http://twitter.com/{{site.twitter_username}}"><div id="twitter" class="social-media"> </div></a>
		<a href="http://facebook.com/{{site.facebook_username}}"><div id="facebook" class="social-media"> </div></a>
		<a href="http://github.com/{{site.github_username}}"><div id="github" class="social-media"> </div></a>
		<h1>shaunalynn<br>duffy</h1>
	</div>
</div>