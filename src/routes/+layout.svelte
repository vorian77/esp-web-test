<script>
	import { APP_NAME, APP_DESCRIPTION } from '$lib/components/constants'
	import { setupIonicBase } from 'ionic-svelte'
	setupIonicBase()
	import '$lib/theme/variables.css'
	import 'ionic-svelte/components/all'
</script>

<svelte:head>
	<title>{APP_NAME}</title>
	<meta name="description" content={APP_DESCRIPTION} /> -->
</svelte:head>

<ion-app>
	<slot />
</ion-app>
