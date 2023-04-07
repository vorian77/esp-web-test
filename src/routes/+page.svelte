<script>
	import { routeToPage } from '$lib/components/nav'
	import { APP_NAME } from '$lib/components/constants'
	//routeToPage('welcome', false)
</script>

<ion-content fullscreen>
	<h1>{APP_NAME}</h1>
	<h2>Temporary Menu</h2>
	<button on:click={() => routeToPage('welcome', false)}>Welcome</button>
	<button on:click={() => routeToPage('auth/login', false)}>Login</button>
	<button on:click={() => routeToPage('auth/signup', false)}>Signup</button>
	<button on:click={() => routeToPage('demo', false)}>Demo</button>
	<button on:click={() => routeToPage('test', false)}>Test</button>
</ion-content>
