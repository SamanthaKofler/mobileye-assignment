<template>
	<header class="outer-container">
    <div class="header inner-container">
		<img @click="reload()" src="./../assets/img/logo_white.png" />
		<div class="social">
			<a @click="reload()"><i class="fab fa-facebook-f"></i></a>
			<a @click="reload()"><i class="fab fa-linkedin-in"></i></a>
			<a @click="reload()"><i class="fab fa-twitter"></i></a>
			<a @click="reload()"><i class="fab fa-youtube"></i></a>
		</div>
    </div>
	</header>
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