<script>
	export let segment;
</script>

<style>
	nav {
		width: 65px;
		height: 100%;
		position: absolute;
		top: 0;
		background-color: #181818;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		border-right: 1px solid grey;
	}

	.logo {
		width: 75px;
		margin-top: 10px;
		margin-left: 3px;
		transition: all .3s;
	}

	.logo:hover {
		transform: rotate(45deg);
	}

	.site-nav {
		display: flex;
		flex-direction: column;
		align-items: center;
		position: relative;
	}

	.site-nav > a {
		margin-bottom: 1rem;
		position: relative;
	}

	.site-nav > a:after {
		content: '';
		font-size: 9px;
		letter-spacing: 2px;
		display: block;
		width: 100%;
		text-align: center;
		opacity: 0;
		transition: all .3s ease-out;
		color: white;
		position: absolute;
		bottom: 15px;
	}

	/* home */
	.icon-home:before {
		content: "home";
		opacity: 1;
		transition: all .3s ease-out;
	}

	.icon-home:hover:before{
		opacity: 0;
	}

	.a-icon-home:hover:after {
		content: "HOME";
		opacity: 1;
	}

	.a-icon-home:hover > i:before {
		opacity: 0;
	}

	/* about - account_circle */
	.icon-about:before {
		content: "account_circle";
		opacity: 1;
		transition: all .3s ease-out;
	}

	.icon-about:hover:before{
		opacity: 0;
	}

	.a-icon-about:hover:after {
		content: "ABOUT";
		opacity: 1;
	}

	.a-icon-about:hover > i:before {
		opacity: 0;
	}

	/* projects - apps */
	.icon-projects:before {
		content: "apps";
		opacity: 1;
		transition: all .3s ease-out;
	}

	.icon-projects:hover:before{
		opacity: 0;
	}

	.a-icon-projects:hover:after {
		content: "PROJECTS";
		opacity: 1;
	}

	.a-icon-projects:hover > i:before {
		opacity: 0;
	}

	a:first-child+a+a:after{
		left: -8px;
	}

	/* uses - phonelink */
	.icon-uses:before {
		content: "phonelink";
		opacity: 1;
		transition: all .3s ease-out;
	}

	.icon-uses:hover:before{
		opacity: 0;
	}

	.a-icon-uses:hover:after {
		content: "USES";
		opacity: 1;
	}

	.a-icon-uses:hover > i:before {
		opacity: 0;
	}

	/* contact - email */
	.icon-contact:before {
		content: "email";
		opacity: 1;
		transition: all .3s ease-out;
	}

	.icon-contact:hover:before{
		opacity: 0;
	}

	.a-icon-contact:hover:after {
		content: "CONTACT";
		opacity: 1;
	}

	.a-icon-contact:hover > i:before {
		opacity: 0;
	}

		a:first-child+a+a+a+a:after{
		left: -7px;
	}

</style>

<nav>
	<a href="." class="logo-wrapper">
		<img src="logo-blueg.png" alt="" class="logo">
	</a>
	<div class="site-nav">
		<a aria-current='{segment === undefined ? "page" : undefined}' href='.' class="a-icon-home">
			<i class="material-icons md-36 md-light icon-home"></i>
		</a>
		<a aria-current='{segment === "about" ? "page" : undefined}' href='about' class="a-icon-about">
			<i class="material-icons md-36 md-light icon-about"></i>
		</a>
		<a aria-current='{segment === "projects" ? "page" : undefined}' href='projects' class="a-icon-projects">
			<i class="material-icons md-36 md-light icon-projects"></i>
		</a>
		<a aria-current='{segment === "uses" ? "page" : undefined}' href='uses' class="a-icon-uses">
			<i class="material-icons md-36 md-light icon-uses"></i>
		</a>
		<a aria-current='{segment === "contact" ? "page" : undefined}' href='contact' class="a-icon-contact">
			<i class="material-icons md-36 md-light icon-contact"></i>
		</a>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<!-- <a rel=prefetch aria-current='{segment === "blog" ? "page" : undefined}' href='blog'>blog</a> -->
	</div>

	<div class="social-icons">
	</div>


</nav>
