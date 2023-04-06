<script>
	import { routeToPage } from '$lib/components/nav'
	import { APP_NAME } from '$lib/components/constants'
</script>

<ion-content fullscreen>
	<h1>Welcome</h1>
	<h2>{APP_NAME}</h2>
	<button on:click={() => routeToPage('auth/login', false)}>Login</button>
	<button on:click={() => routeToPage('auth/signup', false)}>Signup</button>
	<button on:click={() => routeToPage('demo', false)}>Demo</button>
</ion-content>
