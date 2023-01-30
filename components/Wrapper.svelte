<script>
	export let Page = null
	export let rootPath = ''
</script>

<svelte:head>

	<title>Dominion Institute</title>

	<!-- Global site tag (gtag.js) - Google Analytics -->
	<script async src="https://www.googletagmanager.com/gtag/js?id=UA-113064692-3"></script>
	<script>
		window.dataLayer = window.dataLayer || [];
		function gtag(){dataLayer.push(arguments);}
		gtag('js', new Date());

		gtag('config', 'UA-113064692-3');
	</script>

	<meta charset="utf-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="style.css" />

	<link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">
	<link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png">
	<link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png">
	<link rel="manifest" href="site.webmanifest">
	<link rel="mask-icon" href="safari-pinned-tab.svg" color="#5bbad5">
	<meta name="msapplication-TileColor" content="#b91d47">
	<meta name="theme-color" content="#ffffff">

	<link href='https://fonts.googleapis.com/css?family=Vollkorn:400,700' rel='stylesheet' type='text/css'>
</svelte:head>

<nav class="navbar-top">
	<div class="centered-content navbar-top-content">
		<ul>
			<li>
				<a href="{rootPath}">
					<img
						src={rootPath + "images/logo-di.png"}
						alt="Dominion Institute"
					>
				</a>
			</li>
			<li>
				<a href={rootPath + "about.html"}>About</a>
			</li>
			<li>
				<a href="https://donations.biblicalblueprints.org">Give</a>
			</li>
		</ul>
	</div>
</nav>

<div class="centered-content main-content">
	<svelte:component this={Page} />
</div>


<style>
nav {
	--navitem-padding: 16px;
}
.navbar-top {
	background-color: #333333;
}

.navbar-top img {
	height: 32px;
}

.navbar-top-content {
	display: flex;
	align-items: center;
}

.navbar-top ul {
	list-style-type: none;
	padding-left: 0;
	margin: 0;
	margin-left: calc(-1 * var(--navitem-padding));

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
	font-size: 18px;

	padding-left: var(--navitem-padding);
	padding-right: var(--navitem-padding);

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
}

@media (max-width: 680px) {
	nav {
		--navitem-padding: 8px;
	}

	.navbar-top img {
		height: 28px;
	}

	.navbar-top a {
		font-size: 16px;
	}

	.navbar-top li {
		height: 48px;
	}
}

@media (max-width: 500px) {
	.navbar-top img {
		height: 20px;
	}
}

</style>
