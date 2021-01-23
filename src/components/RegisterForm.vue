<template>
<div class="register">
<popup-modal :isHidden="popupIsHidden" @closeModal="closeModal()"/>
<h1>register now</h1>
<div class="form flex wrap justify-center">
<div class="side1 flex column">
  <input type="text" v-model="firstName" required placeholder ="First Name*"/>
  <input type="text" v-model="lastName" required placeholder="Last Name*"/>
  <input type="email" v-model="email" required placeholder="Email*"/>
  <select v-model="country" required>
    <option value="" disabled selected hidden>Country*</option>
    <option value="Israel">Israel</option>
    <option value="USA">USA</option>
    <option value="Switzerland">Switzerland</option>
  </select>
</div>
<div class="side2 flex column">
  <input type="text" v-model="jobTitle" placeholder="Job Title"/>
  <input type="text" v-model="companyName" placeholder="Company Name"/>
   <select v-model="bestDescr">
    <option value="" disabled selected hidden>What Best Describes You?</option>
    <option value="smart">Smart</option>
    <option value="innovative">Innovative</option>
    <option value="fast">Fast</option>
  </select>
</div>
</div>
<div class="checkbox">
  <input type="checkbox" name="checkbox"/>
  <label for="checkbox">Yes, I would like to subscribe to stay connected to the latest Mobileye 
    technologies and industry trends by email and telephone. I can unsubscribe at 
    any time.</label>
    </div>
      <div class="flex justify-center">
    <button @click="submitForm()">register now</button>
    </div>
</div>
</template>

<script>
import PopupModal from './PopupModal.vue';
export default {
	components: { PopupModal },
  name: "RegisterForm",
  data() {
    return {
      firstName: '',
      lastName: '',
      email: '',
      country: '',
      jobTitle: '',
      companyName: '',
      bestDescr: '',
      popupIsHidden: true
    }
  },
  methods: {
    submitForm() {
      console.log(this.country, this.bestDescr)
      if (!this.firstName || !this.lastName || !this.email || !this.country) {
        this.popupIsHidden = false;
        return
      }

      else {
        console.log('submit');
        window.location.reload();
      }
      // this.popupIsHidden = false;
    },
    closeModal() {
            this.popupIsHidden = true;
        }
  },
  created() {
    console.log(this.popupIsHidden)
  }

}
</script>

<style>

</style>