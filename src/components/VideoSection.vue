<template>
	<div class="video-section">
		<div class="video-container flex inner-container">
			<div class="video flex">
				<youtube :video-id="videoId" player-width="400" player-height="250" ></youtube>
			</div>
			<div class="video-txt-container flex column">
				<h3>AUTONOMOUS VEHICLE SAFETY</h3>
				<p class="narrow-line-height">Mobileye, an Intel Company, believes that the most important factor in enabling the wide
					adoption of autonomous vehicles will be agreement upon a common safety standard. We
					have proposed what we are calling Responsibility-Sensitive Safety (RSS) – a mathematical
					model to ensure that the autonomous vehicles of the future will always make safe decisions.
					We are engaging partners across the industry to put safety at the forefront of the
					autonomous discourse – and you are invited to join us.
				</p>
                <button @click="reload()">learn more</button>
			</div>
		</div>
	</div>

</template>

<script>
export default {
	data() {
		return {
			videoId: "EceAB6TUYzo",
		};
	},
	methods: {
			reload() {
			window.location.reload();
		}
	}
};
</script>

<style>
</style>