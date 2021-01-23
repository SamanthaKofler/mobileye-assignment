<template>
	<div class="map-section outer-container">
        <div class="map-container inner-container flex wrap">
		<div class="txt-container flex column">
			<h3>MAPPING THE ROUTE TO THE AUTONOMOUS TOMORROW</h3>
			<p class="narrow-line-height">Mobileye is harnessing the power of the crowd to create the high accuracy maps which are
				essential to making the autonomous future a reality. Trailblazing municipalities around the
				world have begun to retrofit their fleets with Mobileye technology to ensure that their cities
				will be “Autonomous Ready™”. Learn more about how our Road Experience Management™
				(REM™) technology works at our booth: LVCC, North Hall 7511.</p>
			<button @click="reload()">learn more</button>
		</div>
 
        </div>
        <img src="../assets/img/img_1.jpg" />
	</div>

</template>

<script>
export default {
	methods: {
		reload() {
			window.location.reload();
		}
	}
};
</script>

<style>

</style>