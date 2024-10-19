<script>
	import CollapsibleSection from '../../CollapsibleSection.svelte';
</script>

<svelte:head>
	<title>Why Engineering on the Moon is Hard</title>
</svelte:head>

<h1>Why Engineering on the Moon is Hard</h1>
<div class="opacity-60 mb-8">May 2024</div>

<!-- Content Section -->
<p>
	For the last month, I was working on a lunar rover and as I started getting deeper into the project, I discovered that there are many more challenges to build something moon-grade than I thought. Here are some of my findings and a dump of some of the things I considered through the journey.
</p>

<strong>Power</strong>
<p>
	Normally when building a rover or any sort of hardware project, you need to decide what will power it. Whether it’s powered through solar panels, a lithium-ion battery, or a combination of energy sources, this decision is crucial for the operation of what you’re building. For space exploration, the choice becomes more challenging because there are new obstacles.
</p>
<p>
	NASA’s recent rover VIPER, which is planned to launch on Falcon 9 at the end of 2024, is intended to work for 3 months and then just die. This is because we still haven’t solved power on the moon. Solar power or a nuclear reactor are the two main options, but solar isn’t as reliable due to the moon’s long dark days.
</p>

<strong>Computer/Microcontrollers</strong>
<p>
	You can’t just use a Raspberry Pi or Jetson Nano on a moon rover because the moon lacks a magnetic field, exposing electronics to radiation that causes bit flips. Satellites face similar challenges, using error correction methods based on their distance from Earth.
</p>

<strong>Lidars on the Moon</strong>
<p>
	SLAM (Simultaneous Localization and Mapping) is useful for creating maps of unknown environments, and lidars are often used to achieve this. However, lidars generate a significant amount of heat, and traditional Earth cooling methods don't work on the moon. New cooling systems need to be designed for moon-grade lidars.
</p>

<strong>Lunar Regolith</strong>
<p>
	An important consideration for landing on the lunar surface is dealing with lunar regolith, a sandy and sharp material that can damage mechanical parts. One solution I considered was using a swarm of small robots to clear an area for a safe landing pad.
</p>

<strong>Re-Engineering Everything</strong>
<p>
	Many systems we take for granted on Earth must be re-engineered for the moon. From extreme temperature fluctuations to managing abrasive lunar dust, every aspect of technology must be reconsidered.
</p>

<!-- Image Section -->
<div class="images">
	<img src="moon.png" alt="Lunar Rover Concept" class="image-class" />
</div>

<style>
	.images {
		display: flex;
		justify-content: center;
		margin-top: 20px;
	}
	.image-class {
		width: 300px; /* Adjust the size based on your needs */
		height: auto;
	}
</style>

