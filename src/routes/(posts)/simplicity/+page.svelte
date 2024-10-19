<svelte:head>
	<title>Heat Tile Crack Detection Drone</title>
</svelte:head>
<h1>Heat Tile Crack Detection Drone</h1>
<div class="opacity-60 mb-8">July 2024</div>
<p>
	When Starship performs re-entry, a lot of the heat tiles fall off. The tiles are made of ceramic which is a brittle material 
	so when they are placed on the ship, any sort of damage (small cracks) might cause issues during flight. Someone was on a 
	crane manually inspecting and tagging red/green on the tiles during Starship's development. This could be automated with a drone 
	that takes a video of the rocket and uses CV to detect locations of cracks on tiles and generate a color coded map of tiles to inspect and fix. 
	My crack identification drone is a protoptype for this solution to speed up Starship development.
</p>
<p>
	There was 2 parts to this project - hardware and software. I built the drone from scratch mainly for fun and learrning purposes, a prod level 
	version would probably use an off the shelf drone.
</p>
<!-- Adding images at the bottom -->
<div class="images">
	<img src="tile1.png" alt="Description of Image 1" class="image-class" />
	<img src="drone.png" alt="Description of Image 1" class="image-class" />
	<img src="drone2.png" alt="Description of Image 1" class="image-class" />

</div>

<style>
	/* Add some basic styling to manage image size or layout if necessary */
	.images {
		display: flex;
		justify-content: center;
		gap: 10px; /* Space between images */
		margin-top: 20px;
	}

	.image-class {
		width: 200px; /* Adjust based on the size you want */
		height: auto;
	}
</style>