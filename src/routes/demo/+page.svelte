<script>
	import { Geolocation } from '@capacitor/geolocation'
	import { Camera, CameraResultType } from '@capacitor/camera'
	import picture from '$lib/images/shirt.jpg'

	let loc = null
	async function getCurrentPosition() {
		const res = await Geolocation.getCurrentPosition()
		loc = res
	}

	//let picture
	//let picture = '../src/lib/images/pants.jpg'
	let newPicture
	const takePicture = async () => {
		const image = await Camera.getPhoto({
			quality: 90,
			allowEditing: true,
			resultType: CameraResultType.Uri
		})
		newPicture = image.webPath
	}
</script>

<ion-content fullscreen>
	<h1>Original: {picture}</h1>
	<h1>new: {newPicture}</h1>
	<ion-card>
		<ion-title size="large">Ionic - Geolocation</ion-title>
		<p>Your location is:</p>
		<p>Latitude: {loc?.coords.latitude}</p>
		<p>Longitude: {loc?.coords.longitude}</p>
		<ion-button expand="block" on:click={getCurrentPosition}> Get Current Location </ion-button>
	</ion-card>

	<ion-card>
		<ion-title size="large">Ionic - Camera</ion-title>
		<img class="fit-picture" src={newPicture || picture} alt="pic from camera" />
		<ion-button expand="block" on:click={takePicture}>Take Picture</ion-button>
	</ion-card>
</ion-content>

<style>
	ion-title {
		--color: #21a461;
	}
</style>
