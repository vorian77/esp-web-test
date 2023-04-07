<ion-header translucent="true">
	<ion-toolbar>
		<ion-title> Title </ion-title>
	</ion-toolbar>
</ion-header>

<ion-content fullscreen="true">
	<div class="flexbox-container">
		<div class="flexbox-item flexbox-item-1" />
		<div class="flexbox-item flexbox-item-2" />
		<div class="flexbox-item flexbox-item-3">
			<ion-button expand="block" shape="round">Get started</ion-button>
			<ion-button expand="block" shape="round" fill="outline">Log in</ion-button>
		</div>
	</div>
</ion-content>

<ion-footer>
	<p>
		<ion-text>
			By continuing you agree to YO-Baltimore's Terms of Service and Privacy Policy
		</ion-text>
	</p>
</ion-footer>

<style>
	ion-button {
		text-transform: none;
	}
	/* Background Styles */
	/* html {
		height: 100%;
		background-color: #333;
		display: flex;
		flex-direction: column;
		justify-content: center;
	} */

	.flexbox-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		/* position: relative; */
		background-color: yellow;
		height: 100%;
	}

	.flexbox-item {
		position: relative;

		width: 85%;
		margin: 10px;
		border: 3px solid #333;
		background-color: #dfdfdf;
	}

	.flexbox-item-1 {
		min-height: 150px;
	}

	.flexbox-item-2 {
		min-height: 300px;
	}

	.flexbox-item-3 {
		min-height: 90px;
	}

	.flexbox-item::before {
		content: 'Flexbox Item';
		position: absolute;
		color: black;
		font-size: 25px;
		top: 10px;
		left: 15px;
	}
	.flexbox-item::after {
		position: absolute;
		color: black;
		font-size: 25px;
		top: 10px;
		right: 15px;
	}

	.flexbox-item-1::after {
		content: '1';
	}

	.flexbox-item-2::after {
		content: '2';
	}

	.flexbox-item-3::after {
		content: '3';
	}
</style>
