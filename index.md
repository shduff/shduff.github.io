---
layout: default
---

<style>
div#logotype {
	position:fixed;
	right:1em;
	bottom:0;
	font-family:Courier;
	font-size:3em;
}
div.social-media {
	height:1em;
	width:1em;
	display:inline-block;
	border:solid 1px #aaa;
	border-radius:.1em;
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
</style>


<div id="nav">
	<ul>
		<a href=""><li>EDU</li></a>
		<a href=""><li>MUSIC</li></a>
		<a href=""><li>POETRY</li></a>
		<a href=""><li>NOTEBOOK</li></a>
		<a href=""><li>CONTACT</li></a>
	</ul>
</div>

<div id="logotype">
	<h1>shaunalynn duffy</h1>
	<a href="mailto:{{site.email}}"><div id="email" class="social-media"> </div></a>
	<a href="http://twitter.com/{{site.twitter_username}}"><div id="twitter" class="social-media"> </div></a>
	<a href="http://facebook.com/{{site.facebook_username}}"><div id="facebook" class="social-media"> </div></a>
	<a href="http://github.com/{{site.github_username}}"><div id="github" class="social-media"> </div></a>
</div>