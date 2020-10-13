<script>
	export let Page = null
	export let rootPath = ''
</script>

<svelte:head>

	<!-- Global site tag (gtag.js) - Google Analytics -->
	<script async src="https://www.googletagmanager.com/gtag/js?id=UA-113064692-3"></script>
	<script>
		window.dataLayer = window.dataLayer || [];
		function gtag(){dataLayer.push(arguments);}
		gtag('js', new Date());

		gtag('config', 'UA-113064692-3');
	</script>

	<meta charset="utf-8" />
	<link href='https://fonts.googleapis.com/css?family=Vollkorn:400,700' rel='stylesheet' type='text/css'>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="style.css" />

	<link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">
	<link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png">
	<link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png">
	<link rel="manifest" href="site.webmanifest">
	<link rel="mask-icon" href="safari-pinned-tab.svg" color="#5bbad5">
	<meta name="msapplication-TileColor" content="#b91d47">
	<meta name="theme-color" content="#ffffff">

</svelte:head>

<nav class="navbar-top">
	<div class="centered-content navbar-top-content">
		<!-- Josh, can we turn the DI logo into the "Home" link and remove the words? I can't do it, but I'd prefer that for design purposes. -->
		<img
			src={rootPath + "images/logo-di.png"}
			alt="DI logo"
		>
		<ul>
			<li>
				<a href={rootPath + "contact.html"}>About</a>
			</li>
			<li>
				<a href="https://donations.biblicalblueprints.org">Support</a>
			</li>
		</ul>
	</div>
</nav>

<div class="centered-content main-content">
	<svelte:component this={Page} />
</div>


<style>
.navbar-top {
	background-color: #333333;
}

.navbar-top img {
	height: 32px;
	width: 32px;
	margin-right: 16px;
}

.navbar-top-content {
	display: flex;
	align-items: center;
}

.navbar-top ul {
	list-style-type: none;
	padding-left: 0;
	margin: 0;

	display: flex;
}
.navbar-top li {
	height: 64px;

	display: flex;
	align-items: stretch;
}

.navbar-top a {
	color: #fdfdfd;
	text-decoration: none;
	white-space: nowrap;
	font-size: 14px;

	padding-left: 16px;
	padding-right: 16px;

	display: flex;
	align-items: center;

	flex-grow: 1;
}
.navbar-top a:visited {
	color: #fdfdfd;
}

.navbar-top a:hover {
	background-color: #616161;
}

.main-content {
	padding-top: 16px;
	padding-bottom: 32px;
	background-color: #fbfbfb;
}

@media (max-width: 680px) {
	.navbar-top img {
		height: 28px;
		width: 28px;
		margin-right: 16px;
	}

	.navbar-top a {
		font-size: 16px;

		padding-left: 8px;
		padding-right: 8px;
	}

	.navbar-top li {
		height: 48px;
	}
}


</style>
