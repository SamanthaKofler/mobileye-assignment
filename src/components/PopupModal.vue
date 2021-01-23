<template>
	<div
		v-if="!isHidden"
		class="popup">
		<a
			class="close-modal"
			@click="closeModal()">x</a>
		<div class="error-txt">
			<h5>Error!</h5>
			<p>Cannot submit, please fill out all the required fields!</p>
		</div>
	</div>
</template>

<script>
export default {
	props: ["isHidden"],
	methods: {
		closeModal() {
			this.$emit("closeModal");
		},
	},
};
</script>

<style>
</style>