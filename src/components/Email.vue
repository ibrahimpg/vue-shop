<template>
  <div class="emailContainer">
    <div>
      <p>SIGN UP TO RECEIVE EXCLUSIVE DISCOUNTS AND OFFERS</p><br>
    </div>
    <div style="display: flex;">
      <input type="email" required placeholder="YOUR EMAIL">
      <i @click="submitEmail()" class="fas fa-arrow-right"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Email',
  methods: {
    submitEmail(){
      console.log("Submitted!");
    }
  },
}
</script>

<style scoped>
.emailContainer {
  padding: 25px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #42b983;
}

.emailContainer i {
  padding: 17px;
  color: white;
  background-color: rgba(0,0,0,0.8);
}

.emailContainer input {
  height: 50px;
}
</style>
