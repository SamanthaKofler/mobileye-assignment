<template>
	<div class="home outer-container">
		<img class="bgc" src="../assets/img/top_bkg_fill.png" />
		<Header />
    <Hero></Hero>
	<!-- <popup-modal /> -->
	<div class="amnon-register inner-container">
	<Amnon></Amnon>
	<RegisterForm></RegisterForm>
	</div>
	<VideoSection/>
	<MapSection/>
	<Footer />
	</div>
</template>

<script>
import Hero from '../components/Hero.vue';
import Amnon from '../components/Amnon.vue';
import RegisterForm from '../components/RegisterForm.vue';
import VideoSection from '../components/VideoSection.vue';
import MapSection from '../components/MapSection.vue';
import Footer from '../components/Footer.vue';
import Header from '../components/Header.vue';
import PopupModal from '../components/PopupModal.vue';


export default {
	name: "Home",
	components: {
    Hero,
	Amnon,
	RegisterForm,
	VideoSection,
	MapSection,
	Footer,
	Header,
	PopupModal
	},
};
</script>
