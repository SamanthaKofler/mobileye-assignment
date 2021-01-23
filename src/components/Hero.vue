<template>
	<div class="hero outer-container">
        <div class="inner-container">
		<!-- <Header> </Header> -->
		<h2>
			<span>visit mobileye</span> at ces 2019!
		</h2>
		<p class="subtitle">Experience Mobileye’s latest autonomous driving innovations at the Mobileye booth LVCC,
			North Hall, 7511 | January 8th -11th | Las Vegas</p>
		<Timer></Timer>
		<div class="hero-box flex">
			<h3>AN HOUR WITH AMNON
			</h3>
			<div class="box-txt flex column">
				<p>Come hear about the state of our autonomous driving program and how the latest AD and
					ADAS technologies are being delivered globally. Space is limited – register now!
				</p>
                <!-- <hr/> -->
				<p>Tuesday, January 8th at 11am PST | LVCC Room S228 </p>
			</div>
		</div>
        <div class="flex justify-center">
        <button @click="reload()">register now</button>
        </div>
	</div>
    </div>

</template>

<script>
import Timer from "./Timer.vue";
import Header from "./Header.vue";

export default {
	components: {
		Timer,
		Header,
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
