<script>
	import Spinner from '../components/Spinner.svelte'
</script>

<svelte:head>
	<title>Give · Dominion Institute</title>
</svelte:head>

<div id="target">
	<Spinner />
</div>

<p>
	If you've benefited from the ministry of Dominion Institute, please consider donating.  Every gift, no matter the size, is needed and appreciated.
</p>

<p>
	You can make a one-time donation or support us on a recurring basis. All donations to Dominion Institute are tax deductible.
</p>

<p>
	If you want to donate by check, please mail checks to:<br>  
	<br>
	Dominion Institute<br>
	5858 Wenninghoff Rd. Ste. 7<br>
	Omaha, NE 68134  
</p>

<p>
	Please email <a href="mailto:info@dominioninstitute.com">info@dominioninstitute.com</a> with any questions.
</p>

<div>
	<script src="https://cdn.polyfill.io/v2/polyfill.min.js?unknown=polyfill"></script>
	<script src="https://checkout.stripe.com/checkout.js"></script>
	<script src="https://cdn.ravenjs.com/3.19.1/raven.min.js" crossorigin="anonymous"></script>
	<script src="./build.js"></script>
</div>
