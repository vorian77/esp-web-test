<script>
	import { routeToPage } from '$lib/components/nav'
	import logo from '$lib/images/waze-welcome.png'
</script>

<div class="flexbox-container">
	<div class="flexbox-item flexbox-item-1" />
	<div class="flexbox-item flexbox-item-2">
		<img class="logo" src={logo} alt="logo" />
		<p class="text-logo">
			Connect to education and employment at <span class="text-org"
				>Baltimore Youth Opportunity</span
			>
		</p>
	</div>
	<div class="flexbox-item flexbox-item-3">
		<ion-button expand="block" shape="round" on:click={() => routeToPage('auth/signup', false)}
			>Get started</ion-button
		>
		<ion-button
			expand="block"
			shape="round"
			fill="outline"
			on:click={() => routeToPage('auth/login', false)}>Log in</ion-button
		>
	</div>
</div>

<ion-footer>
	<p class="text-footer">
		By continuing you agree to MOED YO Baltimore's <a href="terms@example.com">Terms of Service</a>
		and <a href="privacy@example.com">Privacy Policy</a>
	</p>
</ion-footer>

<style>
	ion-button {
		text-transform: none;
	}
	.logo {
		display: block;
		margin-left: auto;
		margin-right: auto;
		width: 90%;
	}
	.text-logo {
		font-size: 20px;
		font-weight: 700;
		text-align: center;
		border: 3px;
	}
	.text-org {
		font-weight: bolder;
	}
	.text-footer {
		font-size: 12px;
		text-align: center;
		padding: 15px;
		margin: 5px;
	}
	.flexbox-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		height: 100%;
	}
	.flexbox-item {
		position: relative;
		width: 85%;
		margin: 10px;
	}
	.flexbox-item-1 {
		min-height: 30px;
	}
	.flexbox-item-2 {
		min-height: 300px;
	}
	.flexbox-item-3 {
		min-height: 10px;
	}
</style>
